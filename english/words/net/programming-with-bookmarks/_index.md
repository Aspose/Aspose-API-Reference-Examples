---
title: Programming With Bookmarks
linktitle: Programming With Bookmarks
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain access bookmarks, update bookmark data, bookmark table columns, copy bookmarked text, append bookmarked text, create bookmark, show hide bookma
type: docs
weight: 1380
url: /words/net/programming-with-bookmarks/
---
Tutorials contain access bookmarks, update bookmark data, bookmark table columns, copy bookmarked text, append bookmarked text, create bookmark, show hide bookmarks, show hide bookmarked content, untangle row bookmarks, untangle and delete row by bookmark

## Access Bookmarks

```csharp

            
            Document doc = new Document(MyDir + "Bookmarks.docx");
            
            // By index:
            Bookmark bookmark1 = doc.Range.Bookmarks[0];
            // By name:
            Bookmark bookmark2 = doc.Range.Bookmarks["MyBookmark3"];
            
        
```

## Update Bookmark Data

```csharp

            
            Document doc = new Document(MyDir + "Bookmarks.docx");

            Bookmark bookmark = doc.Range.Bookmarks["MyBookmark1"];

            string name = bookmark.Name;
            string text = bookmark.Text;

            bookmark.Name = "RenamedBookmark";
            bookmark.Text = "This is a new bookmarked text.";
            
        
```

## Bookmark Table Columns

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.StartTable();
            
            builder.InsertCell();

            builder.StartBookmark("MyBookmark");

            builder.Write("This is row 1 cell 1");

            builder.InsertCell();
            builder.Write("This is row 1 cell 2");

            builder.EndRow();

            builder.InsertCell();
            builder.Writeln("This is row 2 cell 1");

            builder.InsertCell();
            builder.Writeln("This is row 2 cell 2");

            builder.EndRow();
            builder.EndTable();
            
            builder.EndBookmark("MyBookmark");
            

            
            foreach (Bookmark bookmark in doc.Range.Bookmarks)
            {
                Console.WriteLine("Bookmark: {0}{1}", bookmark.Name, bookmark.IsColumn ? " (Column)" : "");

                if (bookmark.IsColumn)
                {
                    if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row && bookmark.FirstColumn < row.Cells.Count)
                        Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
                }
            }
            
        
```

## Copy Bookmarked Text

```csharp

            Document srcDoc = new Document(MyDir + "Bookmarks.docx");

            // This is the bookmark whose content we want to copy.
            Bookmark srcBookmark = srcDoc.Range.Bookmarks["MyBookmark1"];

            // We will be adding to this document.
            Document dstDoc = new Document();

            // Let's say we will be appended to the end of the body of the last section.
            CompositeNode dstNode = dstDoc.LastSection.Body;

            // If you import multiple times without a single context, it will result in many styles created.
            NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting);

            AppendBookmarkedText(importer, srcBookmark, dstNode);
            
            dstDoc.Save(ArtifactsDir + "WorkingWithBookmarks.CopyBookmarkedText.docx");
        
```

## Append Bookmarked Text

```csharp

            // This is the paragraph that contains the beginning of the bookmark.
            Paragraph startPara = (Paragraph) srcBookmark.BookmarkStart.ParentNode;

            // This is the paragraph that contains the end of the bookmark.
            Paragraph endPara = (Paragraph) srcBookmark.BookmarkEnd.ParentNode;

            if (startPara == null || endPara == null)
                throw new InvalidOperationException(
                    "Parent of the bookmark start or end is not a paragraph, cannot handle this scenario yet.");

            // Limit ourselves to a reasonably simple scenario.
            if (startPara.ParentNode != endPara.ParentNode)
                throw new InvalidOperationException(
                    "Start and end paragraphs have different parents, cannot handle this scenario yet.");

            // We want to copy all paragraphs from the start paragraph up to (and including) the end paragraph,
            // therefore the node at which we stop is one after the end paragraph.
            Node endNode = endPara.NextSibling;

            for (Node curNode = startPara; curNode != endNode; curNode = curNode.NextSibling)
            {
                // This creates a copy of the current node and imports it (makes it valid) in the context
                // of the destination document. Importing means adjusting styles and list identifiers correctly.
                Node newNode = importer.ImportNode(curNode, true);

                dstNode.AppendChild(newNode);
            }
        
```

## Create Bookmark

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.StartBookmark("My Bookmark");
            builder.Writeln("Text inside a bookmark.");

            builder.StartBookmark("Nested Bookmark");
            builder.Writeln("Text inside a NestedBookmark.");
            builder.EndBookmark("Nested Bookmark");

            builder.Writeln("Text after Nested Bookmark.");
            builder.EndBookmark("My Bookmark");

            PdfSaveOptions options = new PdfSaveOptions();
            options.OutlineOptions.BookmarksOutlineLevels.Add("My Bookmark", 1);
            options.OutlineOptions.BookmarksOutlineLevels.Add("Nested Bookmark", 2);

            doc.Save(ArtifactsDir + "WorkingWithBookmarks.CreateBookmark.pdf", options);
            
        
```

## Show Hide Bookmarks

```csharp

            
            Document doc = new Document(MyDir + "Bookmarks.docx");

            ShowHideBookmarkedContent(doc, "MyBookmark1", false);
            
            doc.Save(ArtifactsDir + "WorkingWithBookmarks.ShowHideBookmarks.docx");
            
        
```

## Show Hide Bookmarked Content

```csharp

            Bookmark bm = doc.Range.Bookmarks[bookmarkName];

            DocumentBuilder builder = new DocumentBuilder(doc);
            builder.MoveToDocumentEnd();

            // {IF "{MERGEFIELD bookmark}" = "true" "" ""}
            Field field = builder.InsertField("IF \"", null);
            builder.MoveTo(field.Start.NextSibling);
            builder.InsertField("MERGEFIELD " + bookmarkName + "", null);
            builder.Write("\" = \"true\" ");
            builder.Write("\"");
            builder.Write("\"");
            builder.Write(" \"\"");

            Node currentNode = field.Start;
            bool flag = true;
            while (currentNode != null && flag)
            {
                if (currentNode.NodeType == NodeType.Run)
                    if (currentNode.ToString(SaveFormat.Text).Trim() == "\"")
                        flag = false;

                Node nextNode = currentNode.NextSibling;

                bm.BookmarkStart.ParentNode.InsertBefore(currentNode, bm.BookmarkStart);
                currentNode = nextNode;
            }

            Node endNode = bm.BookmarkEnd;
            flag = true;
            while (currentNode != null && flag)
            {
                if (currentNode.NodeType == NodeType.FieldEnd)
                    flag = false;

                Node nextNode = currentNode.NextSibling;

                bm.BookmarkEnd.ParentNode.InsertAfter(currentNode, endNode);
                endNode = currentNode;
                currentNode = nextNode;
            }

            doc.MailMerge.Execute(new[] { bookmarkName }, new object[] { showHide });
        
```

## Untangle Row Bookmarks

```csharp

            Document doc = new Document(MyDir + "Table column bookmarks.docx");

            // This performs the custom task of putting the row bookmark ends into the same row with the bookmark starts.
            Untangle(doc);

            // Now we can easily delete rows by a bookmark without damaging any other row's bookmarks.
            DeleteRowByBookmark(doc, "ROW2");

            // This is just to check that the other bookmark was not damaged.
            if (doc.Range.Bookmarks["ROW1"].BookmarkEnd == null)
                throw new Exception("Wrong, the end of the bookmark was deleted.");

            doc.Save(ArtifactsDir + "WorkingWithBookmarks.UntangleRowBookmarks.docx");
        
```

## Untangle

```csharp

            foreach (Bookmark bookmark in doc.Range.Bookmarks)
            {
                // Get the parent row of both the bookmark and bookmark end node.
                Row row1 = (Row) bookmark.BookmarkStart.GetAncestor(typeof(Row));
                Row row2 = (Row) bookmark.BookmarkEnd.GetAncestor(typeof(Row));

                // If both rows are found okay, and the bookmark start and end are contained in adjacent rows,
                // move the bookmark end node to the end of the last paragraph in the top row's last cell.
                if (row1 != null && row2 != null && row1.NextSibling == row2)
                    row1.LastCell.LastParagraph.AppendChild(bookmark.BookmarkEnd);
            }
        
```

## Delete Row By Bookmark

```csharp

            Bookmark bookmark = doc.Range.Bookmarks[bookmarkName];

            Row row = (Row) bookmark?.BookmarkStart.GetAncestor(typeof(Row));
            row?.Remove();
        
```


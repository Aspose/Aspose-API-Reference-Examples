---
title: Bookmark Table Columns
linktitle: Bookmark Table Columns
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-bookmarks/bookmark-table-columns/
---




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


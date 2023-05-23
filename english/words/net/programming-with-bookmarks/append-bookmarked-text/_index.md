---
title: Append Bookmarked Text
linktitle: Append Bookmarked Text
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-bookmarks/append-bookmarked-text/
---




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


---
title: Untangle
linktitle: Untangle
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-bookmarks/untangle/
---




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


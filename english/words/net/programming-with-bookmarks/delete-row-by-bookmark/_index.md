---
title: Delete Row By Bookmark
linktitle: Delete Row By Bookmark
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-bookmarks/delete-row-by-bookmark/
---




```csharp

            Bookmark bookmark = doc.Range.Bookmarks[bookmarkName];

            Row row = (Row) bookmark?.BookmarkStart.GetAncestor(typeof(Row));
            row?.Remove();
        
```


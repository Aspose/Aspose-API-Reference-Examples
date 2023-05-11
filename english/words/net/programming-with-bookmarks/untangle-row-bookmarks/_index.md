---
title: Untangle Row Bookmarks
linktitle: Untangle Row Bookmarks
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-bookmarks/untangle-row-bookmarks/
---




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


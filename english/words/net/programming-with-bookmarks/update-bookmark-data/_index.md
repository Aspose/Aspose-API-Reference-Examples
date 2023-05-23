---
title: Update Bookmark Data
linktitle: Update Bookmark Data
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-bookmarks/update-bookmark-data/
---




```csharp

            
            Document doc = new Document(MyDir + "Bookmarks.docx");

            Bookmark bookmark = doc.Range.Bookmarks["MyBookmark1"];

            string name = bookmark.Name;
            string text = bookmark.Text;

            bookmark.Name = "RenamedBookmark";
            bookmark.Text = "This is a new bookmarked text.";
            
        
```


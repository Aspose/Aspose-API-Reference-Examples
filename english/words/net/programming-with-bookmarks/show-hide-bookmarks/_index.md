---
title: Show Hide Bookmarks
linktitle: Show Hide Bookmarks
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-bookmarks/show-hide-bookmarks/
---




```csharp

            
            Document doc = new Document(MyDir + "Bookmarks.docx");

            ShowHideBookmarkedContent(doc, "MyBookmark1", false);
            
            doc.Save(ArtifactsDir + "WorkingWithBookmarks.ShowHideBookmarks.docx");
            
        
```


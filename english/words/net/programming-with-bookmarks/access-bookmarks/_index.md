---
title: Access Bookmarks
linktitle: Access Bookmarks
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-bookmarks/access-bookmarks/
---




```csharp

            
            Document doc = new Document(MyDir + "Bookmarks.docx");
            
            // By index:
            Bookmark bookmark1 = doc.Range.Bookmarks[0];
            // By name:
            Bookmark bookmark2 = doc.Range.Bookmarks["MyBookmark3"];
            
        
```


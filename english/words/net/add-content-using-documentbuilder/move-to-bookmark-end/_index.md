---
title: Move To Bookmark End
linktitle: Move To Bookmark End
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/move-to-bookmark-end/
---




```csharp

            
            Document doc = new Document(MyDir + "Bookmarks.docx");
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.MoveToBookmark("MyBookmark1", false, true);
            builder.Writeln("This is a bookmark.");
            
        
```


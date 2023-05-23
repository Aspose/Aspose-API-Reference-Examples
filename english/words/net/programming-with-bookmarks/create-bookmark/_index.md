---
title: Create Bookmark
linktitle: Create Bookmark
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-bookmarks/create-bookmark/
---




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


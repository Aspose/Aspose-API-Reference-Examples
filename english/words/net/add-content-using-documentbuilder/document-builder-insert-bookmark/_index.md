---
title: Document Builder Insert Bookmark
linktitle: Document Builder Insert Bookmark
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/document-builder-insert-bookmark/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.StartBookmark("FineBookmark");
            builder.Writeln("This is just a fine bookmark.");
            builder.EndBookmark("FineBookmark");

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.DocumentBuilderInsertBookmark.docx");
            
        
```


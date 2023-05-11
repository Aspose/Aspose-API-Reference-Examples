---
title: Insert Document With Builder
linktitle: Insert Document With Builder
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/insert-document-with-builder/
---




```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");
            DocumentBuilder builder = new DocumentBuilder(dstDoc);

            builder.MoveToDocumentEnd();
            builder.InsertBreak(BreakType.PageBreak);

            builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            builder.Document.Save(ArtifactsDir + "JoinAndAppendDocuments.InsertDocumentWithBuilder.docx");
            
        
```


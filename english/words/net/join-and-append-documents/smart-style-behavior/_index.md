---
title: Smart Style Behavior
linktitle: Smart Style Behavior
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/smart-style-behavior/
---




```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");
            DocumentBuilder builder = new DocumentBuilder(dstDoc);
            
            builder.MoveToDocumentEnd();
            builder.InsertBreak(BreakType.PageBreak);

            ImportFormatOptions options = new ImportFormatOptions { SmartStyleBehavior = true };

            builder.InsertDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);
            builder.Document.Save(ArtifactsDir + "JoinAndAppendDocuments.SmartStyleBehavior.docx");
            
        
```


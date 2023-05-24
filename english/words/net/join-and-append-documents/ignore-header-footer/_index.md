---
title: Ignore Header Footer
linktitle: Ignore Header Footer
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/ignore-header-footer/
---




```csharp

            
            Document srcDocument = new Document(MyDir + "Document source.docx");
            Document dstDocument = new Document(MyDir + "Northwind traders.docx");

            ImportFormatOptions importFormatOptions = new ImportFormatOptions { IgnoreHeaderFooter = false };

            dstDocument.AppendDocument(srcDocument, ImportFormatMode.KeepSourceFormatting, importFormatOptions);
            
            dstDocument.Save(ArtifactsDir + "JoinAndAppendDocuments.IgnoreHeaderFooter.docx");
            
        
```


---
title: Smart Style Behavior
linktitle: Smart Style Behavior
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/smart-style-behavior/
---
### Sample source code for Smart Style Behavior using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDoc = new Document(dataDir + "Document source.docx");
            Document dstDoc = new Document(dataDir + "Northwind traders.docx");
            DocumentBuilder builder = new DocumentBuilder(dstDoc);
            builder.MoveToDocumentEnd();
            builder.InsertBreak(BreakType.PageBreak);
            ImportFormatOptions options = new ImportFormatOptions { SmartStyleBehavior = true };
            builder.InsertDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);
            builder.Document.Save(dataDir + "JoinAndAppendDocuments.SmartStyleBehavior.docx");
```
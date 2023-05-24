---
title: Insert Document With Builder
linktitle: Insert Document With Builder
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/insert-document-with-builder/
---
### Sample source code for Insert Document With Builder using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDoc = new Document(dataDir + "Document source.docx");
            Document dstDoc = new Document(dataDir + "Northwind traders.docx");
            DocumentBuilder builder = new DocumentBuilder(dstDoc);
            builder.MoveToDocumentEnd();
            builder.InsertBreak(BreakType.PageBreak);
            builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            builder.Document.Save(dataDir + "JoinAndAppendDocuments.InsertDocumentWithBuilder.docx");
```
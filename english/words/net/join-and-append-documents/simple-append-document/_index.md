---
title: Simple Append Document
linktitle: Simple Append Document
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/simple-append-document/
---
### Sample source code for Simple Append Document using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDoc = new Document(dataDir + "Document source.docx");
            Document dstDoc = new Document(dataDir + "Northwind traders.docx");
            // Append the source document to the destination document using no extra options.
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            dstDoc.Save(dataDir + "JoinAndAppendDocuments.SimpleAppendDocument.docx");
```
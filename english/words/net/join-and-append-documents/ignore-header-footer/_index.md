---
title: Ignore Header Footer
linktitle: Ignore Header Footer
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/ignore-header-footer/
---
### Sample source code for Ignore Header Footer using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDocument = new Document(dataDir + "Document source.docx");
            Document dstDocument = new Document(dataDir + "Northwind traders.docx");
            ImportFormatOptions importFormatOptions = new ImportFormatOptions { IgnoreHeaderFooter = false };
            dstDocument.AppendDocument(srcDocument, ImportFormatMode.KeepSourceFormatting, importFormatOptions);
            dstDocument.Save(dataDir + "JoinAndAppendDocuments.IgnoreHeaderFooter.docx");
```
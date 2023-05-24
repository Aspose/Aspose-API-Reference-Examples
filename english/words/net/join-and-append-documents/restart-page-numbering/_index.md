---
title: Restart Page Numbering
linktitle: Restart Page Numbering
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/restart-page-numbering/
---
### Sample source code for Restart Page Numbering using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDoc = new Document(dataDir + "Document source.docx");
            Document dstDoc = new Document(dataDir + "Northwind traders.docx");
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.NewPage;
            srcDoc.FirstSection.PageSetup.RestartPageNumbering = true;
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            dstDoc.Save(dataDir + "JoinAndAppendDocuments.RestartPageNumbering.docx");
```
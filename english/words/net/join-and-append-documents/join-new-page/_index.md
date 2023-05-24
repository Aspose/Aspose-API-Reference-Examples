---
title: Join New Page
linktitle: Join New Page
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/join-new-page/
---
### Sample source code for Join New Page using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDoc = new Document(dataDir + "Document source.docx");
            Document dstDoc = new Document(dataDir + "Northwind traders.docx");
            // Set the appended document to start on a new page.
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.NewPage;
            // Append the source document using the original styles found in the source document.
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            dstDoc.Save(dataDir + "JoinAndAppendDocuments.JoinNewPage.docx");
```
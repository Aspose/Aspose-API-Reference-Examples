---
title: Join Continuous
linktitle: Join Continuous
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/join-continuous/
---
### Sample source code for Join Continuous using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDoc = new Document(dataDir + "Document source.docx");
            Document dstDoc = new Document(dataDir + "Northwind traders.docx");
            // Make the document appear straight after the destination documents content.
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.Continuous;
            // Append the source document using the original styles found in the source document.
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            dstDoc.Save(dataDir + "JoinAndAppendDocuments.JoinContinuous.docx");
```
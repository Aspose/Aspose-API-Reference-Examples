---
title: List Keep Source Formatting
linktitle: List Keep Source Formatting
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/list-keep-source-formatting/
---
### Sample source code for List Keep Source Formatting using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDoc = new Document(dataDir + "Document source.docx");
            Document dstDoc = new Document(dataDir + "Document destination with list.docx");
            // Append the content of the document so it flows continuously.
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.Continuous;
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            dstDoc.Save(dataDir + "JoinAndAppendDocuments.ListKeepSourceFormatting.docx");
```
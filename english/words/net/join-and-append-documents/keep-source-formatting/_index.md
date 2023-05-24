---
title: Keep Source Formatting
linktitle: Keep Source Formatting
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/keep-source-formatting/
---
### Sample source code for Keep Source Formatting using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document dstDoc = new Document();
            dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");
            Document srcDoc = new Document();
            srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");
            // Append the source document to the destination document.
            // Pass format mode to retain the original formatting of the source document when importing it.
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            dstDoc.Save(dataDir + "JoinAndAppendDocuments.KeepSourceFormatting.docx");
```
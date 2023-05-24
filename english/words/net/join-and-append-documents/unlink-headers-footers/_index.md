---
title: Unlink Headers Footers
linktitle: Unlink Headers Footers
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/unlink-headers-footers/
---
### Sample source code for Unlink Headers Footers using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDoc = new Document(dataDir + "Document source.docx");
            Document dstDoc = new Document(dataDir + "Northwind traders.docx");
            // Unlink the headers and footers in the source document to stop this
            // from continuing the destination document's headers and footers.
            srcDoc.FirstSection.HeadersFooters.LinkToPrevious(false);
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            dstDoc.Save(dataDir + "JoinAndAppendDocuments.UnlinkHeadersFooters.docx");
```
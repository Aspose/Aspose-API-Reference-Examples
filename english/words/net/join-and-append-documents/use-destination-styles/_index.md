---
title: Use Destination Styles
linktitle: Use Destination Styles
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/use-destination-styles/
---
### Sample source code for Use Destination Styles using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDoc = new Document(dataDir + "Document source.docx");
            Document dstDoc = new Document(dataDir + "Northwind traders.docx");
            // Append the source document using the styles of the destination document.
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles);
            dstDoc.Save(dataDir + "JoinAndAppendDocuments.UseDestinationStyles.docx");
```
---
title: Update Page Layout
linktitle: Update Page Layout
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/update-page-layout/
---
### Sample source code for Update Page Layout using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDoc = new Document(dataDir + "Document source.docx");
            Document dstDoc = new Document(dataDir + "Northwind traders.docx");
            // If the destination document is rendered to PDF, image etc.
            // or UpdatePageLayout is called before the source document. Is appended,
            // then any changes made after will not be reflected in the rendered output
            dstDoc.UpdatePageLayout();
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            // For the changes to be updated to rendered output, UpdatePageLayout must be called again.
            // If not called again, the appended document will not appear in the output of the next rendering.
            dstDoc.UpdatePageLayout();
            dstDoc.Save(dataDir + "JoinAndAppendDocuments.UpdatePageLayout.docx");
```
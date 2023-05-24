---
title: Append Document To Blank
linktitle: Append Document To Blank
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/append-document-to-blank/
---
### Sample source code for Append Document To Blank using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDoc = new Document(dataDir + "Document source.docx");
            Document dstDoc = new Document();
            // The destination document is not empty, often causing a blank page to appear before the appended document.
            // This is due to the base document having an empty section and the new document being started on the next page.
            // Remove all content from the destination document before appending.
            dstDoc.RemoveAllChildren();
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            dstDoc.Save(dataDir + "JoinAndAppendDocuments.AppendDocumentToBlank.docx");
```
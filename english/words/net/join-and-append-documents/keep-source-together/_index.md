---
title: Keep Source Together
linktitle: Keep Source Together
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/keep-source-together/
---
### Sample source code for Keep Source Together using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDoc = new Document(dataDir + "Document source.docx");
            Document dstDoc = new Document(dataDir + "Document destination with list.docx");
            // Set the source document to appear straight after the destination document's content.
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.Continuous;
            foreach (Paragraph para in srcDoc.GetChildNodes(NodeType.Paragraph, true))
            {
                para.ParagraphFormat.KeepWithNext = true;
            }
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            dstDoc.Save(dataDir + "JoinAndAppendDocuments.KeepSourceTogether.docx");
```
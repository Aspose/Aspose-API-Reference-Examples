---
title: Rich Text Box Content Control
linktitle: Rich Text Box Content Control
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/rich-text-box-content-control/
---
### Sample source code for Rich Text Box Content Control using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            StructuredDocumentTag sdtRichText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
            Paragraph para = new Paragraph(doc);
            Run run = new Run(doc);
            run.Text = "Hello World";
            run.Font.Color = Color.Green;
            para.Runs.Add(run);
            sdtRichText.ChildNodes.Add(para);
            doc.FirstSection.Body.AppendChild(sdtRichText);
            doc.Save(dataDir + "WorkingWithSdt.RichTextBoxContentControl.docx");
```
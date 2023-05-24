---
title: Set Content Control Style
linktitle: Set Content Control Style
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/set-content-control-style/
---
### Sample source code for Set Content Control Style using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Structured document tags.docx");
            StructuredDocumentTag sdt = (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);
            Style style = doc.Styles[StyleIdentifier.Quote];
            sdt.Style = style;
            doc.Save(dataDir + "WorkingWithSdt.SetContentControlStyle.docx");
```
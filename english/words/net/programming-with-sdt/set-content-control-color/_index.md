---
title: Set Content Control Color
linktitle: Set Content Control Color
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/set-content-control-color/
---
### Sample source code for Set Content Control Color using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Structured document tags.docx");
            StructuredDocumentTag sdt = (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);
            sdt.Color = Color.Red;
            doc.Save(dataDir + "WorkingWithSdt.SetContentControlColor.docx");
```
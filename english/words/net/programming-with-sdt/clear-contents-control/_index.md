---
title: Clear Contents Control
linktitle: Clear Contents Control
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/clear-contents-control/
---
### Sample source code for Clear Contents Control using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Structured document tags.docx");
            StructuredDocumentTag sdt = (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);
            sdt.Clear();
            doc.Save(dataDir + "WorkingWithSdt.ClearContentsControl.doc");
```
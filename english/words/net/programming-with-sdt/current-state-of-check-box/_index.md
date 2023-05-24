---
title: Current State Of Check Box
linktitle: Current State Of Check Box
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/current-state-of-check-box/
---
### Sample source code for Current State Of Check Box using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Structured document tags.docx");
            // Get the first content control from the document.
            StructuredDocumentTag sdtCheckBox =
                (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);
            if (sdtCheckBox.SdtType == SdtType.Checkbox)
                sdtCheckBox.Checked = true;
            doc.Save(dataDir + "WorkingWithSdt.CurrentStateOfCheckBox.docx");
```
---
title: Current State Of Check Box
linktitle: Current State Of Check Box
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/current-state-of-check-box/
---




```csharp

            
            Document doc = new Document(MyDir + "Structured document tags.docx");
            
            // Get the first content control from the document.
            StructuredDocumentTag sdtCheckBox =
                (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

            if (sdtCheckBox.SdtType == SdtType.Checkbox)
                sdtCheckBox.Checked = true;

            doc.Save(ArtifactsDir + "WorkingWithSdt.CurrentStateOfCheckBox.docx");
            
        
```


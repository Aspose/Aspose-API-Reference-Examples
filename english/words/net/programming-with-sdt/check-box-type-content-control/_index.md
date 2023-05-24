---
title: Check Box Type Content Control
linktitle: Check Box Type Content Control
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/check-box-type-content-control/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            StructuredDocumentTag sdtCheckBox = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
            builder.InsertNode(sdtCheckBox);
            
            doc.Save(ArtifactsDir + "WorkingWithSdt.CheckBoxTypeContentControl.docx", SaveFormat.Docx);
            
        
```


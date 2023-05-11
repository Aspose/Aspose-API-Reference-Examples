---
title: Measure Unit
linktitle: Measure Unit
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-odtsaveoptions/measure-unit/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            // Open Office uses centimeters when specifying lengths, widths and other measurable formatting
            // and content properties in documents whereas MS Office uses inches.
            OdtSaveOptions saveOptions = new OdtSaveOptions { MeasureUnit = OdtSaveMeasureUnit.Inches };

            doc.Save(ArtifactsDir + "WorkingWithOdtSaveOptions.MeasureUnit.odt", saveOptions);
            
        
```


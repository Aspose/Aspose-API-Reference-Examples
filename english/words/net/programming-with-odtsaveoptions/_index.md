---
title: Programming With Odtsaveoptions
linktitle: Programming With Odtsaveoptions
second_title: Aspose.Words for .NET API Reference
description: Examples contain measure unit
type: docs
weight: 1650
url: /words/net/programming-with-odtsaveoptions/
---
Examples contain measure unit

## Measure Unit

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            // Open Office uses centimeters when specifying lengths, widths and other measurable formatting
            // and content properties in documents whereas MS Office uses inches.
            OdtSaveOptions saveOptions = new OdtSaveOptions { MeasureUnit = OdtSaveMeasureUnit.Inches };

            doc.Save(ArtifactsDir + "WorkingWithOdtSaveOptions.MeasureUnit.odt", saveOptions);
            
        
```


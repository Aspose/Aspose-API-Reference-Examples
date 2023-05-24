---
title: Add Corners Snipped
linktitle: Add Corners Snipped
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-shapes/add-corners-snipped/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertShape(ShapeType.TopCornersSnipped, 50, 50);

            OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
            {
                Compliance = OoxmlCompliance.Iso29500_2008_Transitional
            };

            doc.Save(ArtifactsDir + "WorkingWithShapes.AddCornersSnipped.docx", saveOptions);
            
        
```


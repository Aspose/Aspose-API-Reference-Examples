---
title: Add Corners Snipped
linktitle: Add Corners Snipped
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-shapes/add-corners-snipped/
---
### Sample source code for Add Corners Snipped using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            builder.InsertShape(ShapeType.TopCornersSnipped, 50, 50);
            OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
            {
                Compliance = OoxmlCompliance.Iso29500_2008_Transitional
            };
            doc.Save(dataDir + "WorkingWithShapes.AddCornersSnipped.docx", saveOptions);
```
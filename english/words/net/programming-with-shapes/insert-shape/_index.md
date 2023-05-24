---
title: Insert Shape
linktitle: Insert Shape
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-shapes/insert-shape/
---
### Sample source code for Insert Shape using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertShape(ShapeType.TextBox, RelativeHorizontalPosition.Page, 100,
                RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);
            shape.Rotation = 30.0;
            builder.Writeln();
            shape = builder.InsertShape(ShapeType.TextBox, 50, 50);
            shape.Rotation = 30.0;
            OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx)
            {
                Compliance = OoxmlCompliance.Iso29500_2008_Transitional
            };
            doc.Save(dataDir + "WorkingWithShapes.InsertShape.docx", saveOptions);
```
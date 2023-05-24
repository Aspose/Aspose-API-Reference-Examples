---
title: Add Group Shape
linktitle: Add Group Shape
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-shapes/add-group-shape/
---
### Sample source code for Add Group Shape using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            doc.EnsureMinimum();
            GroupShape groupShape = new GroupShape(doc);
            Shape accentBorderShape = new Shape(doc, ShapeType.AccentBorderCallout1) { Width = 100, Height = 100 };
            groupShape.AppendChild(accentBorderShape);
            Shape actionButtonShape = new Shape(doc, ShapeType.ActionButtonBeginning)
            {
                Left = 100, Width = 100, Height = 200
            };
            groupShape.AppendChild(actionButtonShape);
            groupShape.Width = 200;
            groupShape.Height = 200;
            groupShape.CoordSize = new Size(200, 200);
            DocumentBuilder builder = new DocumentBuilder(doc);
            builder.InsertNode(groupShape);
            doc.Save(dataDir + "WorkingWithShapes.AddGroupShape.docx");
```
---
title: Layout In Cell
linktitle: Layout In Cell
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-shapes/layout-in-cell/
---
### Sample source code for Layout In Cell using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            builder.StartTable();
            builder.RowFormat.Height = 100;
            builder.RowFormat.HeightRule = HeightRule.Exactly;
            for (int i = 0; i < 31; i++)
            {
                if (i != 0 && i % 7 == 0) builder.EndRow();
                builder.InsertCell();
                builder.Write("Cell contents");
            }
            builder.EndTable();
            Shape watermark = new Shape(doc, ShapeType.TextPlainText)
            {
                RelativeHorizontalPosition = RelativeHorizontalPosition.Page,
                RelativeVerticalPosition = RelativeVerticalPosition.Page,
                IsLayoutInCell = true, // Display the shape outside of the table cell if it will be placed into a cell.
                Width = 300,
                Height = 70,
                HorizontalAlignment = HorizontalAlignment.Center,
                VerticalAlignment = VerticalAlignment.Center,
                Rotation = -40
            };
            watermark.FillColor = Color.Gray;
            watermark.StrokeColor = Color.Gray;
            watermark.TextPath.Text = "watermarkText";
            watermark.TextPath.FontFamily = "Arial";
            watermark.Name = $"WaterMark_{Guid.NewGuid()}";
            watermark.WrapType = WrapType.None;
            Run run = doc.GetChildNodes(NodeType.Run, true)[doc.GetChildNodes(NodeType.Run, true).Count - 1] as Run;
            builder.MoveTo(run);
            builder.InsertNode(watermark);
            doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
            doc.Save(dataDir + "WorkingWithShapes.LayoutInCell.docx");
```
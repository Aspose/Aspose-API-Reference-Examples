---
title: Tick Multi Line Label Alignment
linktitle: Tick Multi Line Label Alignment
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/tick-multi-line-label-alignment/
---
### Sample source code for Tick Multi Line Label Alignment using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
            ChartAxis axis = shape.Chart.AxisX;
            // This property has effect only for multi-line labels.
            axis.TickLabelAlignment = ParagraphAlignment.Right;
            doc.Save(dataDir + "WorkingWithCharts.TickMultiLineLabelAlignment.docx");
```
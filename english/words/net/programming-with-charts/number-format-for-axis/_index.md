---
title: Number Format For Axis
linktitle: Number Format For Axis
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/number-format-for-axis/
---
### Sample source code for Number Format For Axis using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
            Chart chart = shape.Chart;
            chart.Series.Clear();
            chart.Series.Add("Aspose Series 1",
                new string[] { "Item 1", "Item 2", "Item 3", "Item 4", "Item 5" },
                new double[] { 1900000, 850000, 2100000, 600000, 1500000 });
            chart.AxisY.NumberFormat.FormatCode = "#,##0";
            doc.Save(dataDir + "WorkingWithCharts.NumberFormatForAxis.docx");
```
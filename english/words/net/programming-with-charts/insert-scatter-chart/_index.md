---
title: Insert Scatter Chart
linktitle: Insert Scatter Chart
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/insert-scatter-chart/
---
### Sample source code for Insert Scatter Chart using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
            Chart chart = shape.Chart;
            chart.Series.Add("Aspose Series 1", new double[] { 0.7, 1.8, 2.6 }, new double[] { 2.7, 3.2, 0.8 });
            doc.Save(dataDir + "WorkingWithCharts.InsertScatterChart.docx");
```
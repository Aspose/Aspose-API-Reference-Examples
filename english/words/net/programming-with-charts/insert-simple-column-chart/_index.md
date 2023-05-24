---
title: Insert Simple Column Chart
linktitle: Insert Simple Column Chart
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/insert-simple-column-chart/
---
### Sample source code for Insert Simple Column Chart using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            // You can specify different chart types and sizes.
            Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
            Chart chart = shape.Chart;
            ChartSeriesCollection seriesColl = chart.Series;
            Console.WriteLine(seriesColl.Count);
            // Delete default generated series.
            seriesColl.Clear();
            // Create category names array, in this tutorial we have two categories.
            string[] categories = new string[] { "Category 1", "Category 2" };
            // Please note, data arrays must not be empty and arrays must be the same size.
            seriesColl.Add("Aspose Series 1", categories, new double[] { 1, 2 });
            seriesColl.Add("Aspose Series 2", categories, new double[] { 3, 4 });
            seriesColl.Add("Aspose Series 3", categories, new double[] { 5, 6 });
            seriesColl.Add("Aspose Series 4", categories, new double[] { 7, 8 });
            seriesColl.Add("Aspose Series 5", categories, new double[] { 9, 10 });
            doc.Save(dataDir + "WorkingWithCharts.InsertSimpleColumnChart.docx");
```
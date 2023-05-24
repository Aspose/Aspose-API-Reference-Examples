---
title: Insert Area Chart
linktitle: Insert Area Chart
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/insert-area-chart/
---
### Sample source code for Insert Area Chart using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertChart(ChartType.Area, 432, 252);
            Chart chart = shape.Chart;
            chart.Series.Add("Aspose Series 1", new []
                {
                    new DateTime(2002, 05, 01),
                    new DateTime(2002, 06, 01),
                    new DateTime(2002, 07, 01),
                    new DateTime(2002, 08, 01),
                    new DateTime(2002, 09, 01)
                }, 
                new double[] { 32, 32, 28, 12, 15 });
            doc.Save(dataDir + "WorkingWithCharts.InsertAreaChart.docx");
```
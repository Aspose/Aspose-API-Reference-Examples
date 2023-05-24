---
title: Single Chart Data Point
linktitle: Single Chart Data Point
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/single-chart-data-point/
---
### Sample source code for Single Chart Data Point using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
            Chart chart = shape.Chart;
            ChartSeries series0 = chart.Series[0];
            ChartSeries series1 = chart.Series[1];
            ChartDataPointCollection dataPointCollection = series0.DataPoints;
            ChartDataPoint dataPoint00 = dataPointCollection[0];
            ChartDataPoint dataPoint01 = dataPointCollection[1];
            dataPoint00.Explosion = 50;
            dataPoint00.Marker.Symbol = MarkerSymbol.Circle;
            dataPoint00.Marker.Size = 15;
            dataPoint01.Marker.Symbol = MarkerSymbol.Diamond;
            dataPoint01.Marker.Size = 20;
            ChartDataPoint dataPoint12 = series1.DataPoints[2];
            dataPoint12.InvertIfNegative = true;
            dataPoint12.Marker.Symbol = MarkerSymbol.Star;
            dataPoint12.Marker.Size = 20;
            doc.Save(dataDir + "WorkingWithCharts.SingleChartDataPoint.docx");
```
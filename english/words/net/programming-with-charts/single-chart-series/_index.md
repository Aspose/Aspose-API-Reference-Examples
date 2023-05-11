---
title: Single Chart Series
linktitle: Single Chart Series
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/single-chart-series/
---




```csharp

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Shape shape = builder.InsertChart(ChartType.Line, 432, 252);

            Chart chart = shape.Chart;

            
            ChartSeries series0 = chart.Series[0];
            ChartSeries series1 = chart.Series[1];

            series0.Name = "Chart Series Name 1";
            series1.Name = "Chart Series Name 2";

            // You can also specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines.
            series0.Smooth = true;
            series1.Smooth = true;
            

            
            // Specifies whether by default the parent element shall inverts its colors if the value is negative.
            series0.InvertIfNegative = true;

            series0.Marker.Symbol = MarkerSymbol.Circle;
            series0.Marker.Size = 15;

            series1.Marker.Symbol = MarkerSymbol.Star;
            series1.Marker.Size = 10;
            

            doc.Save(ArtifactsDir + "WorkingWithCharts.SingleChartSeries.docx");
        
```


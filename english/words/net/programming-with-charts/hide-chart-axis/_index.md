---
title: Hide Chart Axis
linktitle: Hide Chart Axis
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/hide-chart-axis/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

            Chart chart = shape.Chart;
            
            chart.Series.Clear();
            
            chart.Series.Add("Aspose Series 1",
                new string[] { "Item 1", "Item 2", "Item 3", "Item 4", "Item 5" },
                new double[] { 1.2, 0.3, 2.1, 2.9, 4.2 });
            
            chart.AxisY.Hidden = true;

            doc.Save(ArtifactsDir + "WorkingWithCharts.HideChartAxis.docx");
            
        
```


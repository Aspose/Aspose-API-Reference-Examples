---
title: Interval Unit Between Labels On Axis
linktitle: Interval Unit Between Labels On Axis
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/interval-unit-between-labels-on-axis/
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

            chart.AxisX.TickLabelSpacing = 2;

            doc.Save(ArtifactsDir + "WorkingWithCharts.IntervalUnitBetweenLabelsOnAxis.docx");
            
        
```

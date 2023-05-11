---
title: Insert Scatter Chart
linktitle: Insert Scatter Chart
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/insert-scatter-chart/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);

            Chart chart = shape.Chart;
            chart.Series.Add("Aspose Series 1", new double[] { 0.7, 1.8, 2.6 }, new double[] { 2.7, 3.2, 0.8 });

            doc.Save(ArtifactsDir + "WorkingWithCharts.InsertScatterChart.docx");
            
        
```


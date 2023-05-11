---
title: Insert Column Chart
linktitle: Insert Column Chart
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/insert-column-chart/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

            Chart chart = shape.Chart;
            chart.Series.Add("Aspose Series 1", new string[] { "Category 1", "Category 2" }, new double[] { 1, 2 });

            doc.Save(ArtifactsDir + "WorkingWithCharts.InsertColumnChart.docx");
            
        
```


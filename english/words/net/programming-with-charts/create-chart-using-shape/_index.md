---
title: Create Chart Using Shape
linktitle: Create Chart Using Shape
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/create-chart-using-shape/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Shape shape = builder.InsertChart(ChartType.Line, 432, 252);

            Chart chart = shape.Chart;
            chart.Title.Show = true;
            chart.Title.Text = "Line Chart Title";
            chart.Title.Overlay = false;

            // Please note if null or empty value is specified as title text, auto generated title will be shown.

            chart.Legend.Position = LegendPosition.Left;
            chart.Legend.Overlay = true;
            
            doc.Save(ArtifactsDir + "WorkingWithCharts.CreateChartUsingShape.docx");
            
        
```


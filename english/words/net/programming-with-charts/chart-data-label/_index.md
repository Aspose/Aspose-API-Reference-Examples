---
title: Chart Data Label
linktitle: Chart Data Label
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/chart-data-label/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Shape shape = builder.InsertChart(ChartType.Bar, 432, 252);

            Chart chart = shape.Chart;
            ChartSeries series0 = shape.Chart.Series[0];

            ChartDataLabelCollection labels = series0.DataLabels;
            labels.ShowLegendKey = true;
            // By default, when you add data labels to the data points in a pie chart, leader lines are displayed for data labels that are
            // positioned far outside the end of data points. Leader lines create a visual connection between a data label and its 
            // corresponding data point.
            labels.ShowLeaderLines = true;
            labels.ShowCategoryName = false;
            labels.ShowPercentage = false;
            labels.ShowSeriesName = true;
            labels.ShowValue = true;
            labels.Separator = "/";
            labels.ShowValue = true;
            
            doc.Save(ArtifactsDir + "WorkingWithCharts.ChartDataLabel.docx");
            
        
```


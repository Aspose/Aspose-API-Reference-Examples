---
title: Default Options For Data Labels
linktitle: Default Options For Data Labels
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/default-options-for-data-labels/
---
### Sample source code for Default Options For Data Labels using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertChart(ChartType.Pie, 432, 252);
            Chart chart = shape.Chart;
            chart.Series.Clear();
            ChartSeries series = chart.Series.Add("Aspose Series 1",
                new string[] { "Category 1", "Category 2", "Category 3" },
                new double[] { 2.7, 3.2, 0.8 });
            ChartDataLabelCollection labels = series.DataLabels;
            labels.ShowPercentage = true;
            labels.ShowValue = true;
            labels.ShowLeaderLines = false;
            labels.Separator = " - ";
            doc.Save(dataDir + "WorkingWithCharts.DefaultOptionsForDataLabels.docx");
```
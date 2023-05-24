---
title: Format Number Of Data Label
linktitle: Format Number Of Data Label
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/format-number-of-data-label/
---
### Sample source code for Format Number Of Data Label using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
            Chart chart = shape.Chart;
            chart.Title.Text = "Data Labels With Different Number Format";
            // Delete default generated series.
            chart.Series.Clear();
            ChartSeries series1 = chart.Series.Add("Aspose Series 1", 
                new string[] { "Category 1", "Category 2", "Category 3" }, 
                new double[] { 2.5, 1.5, 3.5 });
            series1.HasDataLabels = true;
            series1.DataLabels.ShowValue = true;
            series1.DataLabels[0].NumberFormat.FormatCode = "\"$\"#,##0.00";
            series1.DataLabels[1].NumberFormat.FormatCode = "dd/mm/yyyy";
            series1.DataLabels[2].NumberFormat.FormatCode = "0.00%";
            // Or you can set format code to be linked to a source cell,
            // in this case NumberFormat will be reset to general and inherited from a source cell.
            series1.DataLabels[2].NumberFormat.IsLinkedToSource = true;
            doc.Save(dataDir + "WorkingWithCharts.FormatNumberOfDataLabel.docx");
```
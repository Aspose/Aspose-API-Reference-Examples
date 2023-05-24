---
title: Define XYAxis Properties
linktitle: Define XYAxis Properties
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-charts/define-xyaxis-properties/
---
### Sample source code for Define XYAxis Properties using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            // Insert chart
            Shape shape = builder.InsertChart(ChartType.Area, 432, 252);
            Chart chart = shape.Chart;
            chart.Series.Clear();
            chart.Series.Add("Aspose Series 1",
                new DateTime[]
                {
                    new DateTime(2002, 01, 01), new DateTime(2002, 06, 01), new DateTime(2002, 07, 01),
                    new DateTime(2002, 08, 01), new DateTime(2002, 09, 01)
                },
                new double[] { 640, 320, 280, 120, 150 });
            ChartAxis xAxis = chart.AxisX;
            ChartAxis yAxis = chart.AxisY;
            // Change the X axis to be category instead of date, so all the points will be put with equal interval on the X axis.
            xAxis.CategoryType = AxisCategoryType.Category;
            xAxis.Crosses = AxisCrosses.Custom;
            xAxis.CrossesAt = 3; // Measured in display units of the Y axis (hundreds).
            xAxis.ReverseOrder = true;
            xAxis.MajorTickMark = AxisTickMark.Cross;
            xAxis.MinorTickMark = AxisTickMark.Outside;
            xAxis.TickLabelOffset = 200;
            yAxis.TickLabelPosition = AxisTickLabelPosition.High;
            yAxis.MajorUnit = 100;
            yAxis.MinorUnit = 50;
            yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
            yAxis.Scaling.Minimum = new AxisBound(100);
            yAxis.Scaling.Maximum = new AxisBound(700);
            doc.Save(dataDir + "WorkingWithCharts.DefineXYAxisProperties.docx");
```
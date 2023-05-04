---
title: lnk Annotation Line Width
linktitle: lnk Annotation Line Width
second_title: Aspose.PDF for .NET API Reference
description: The example shows how to lnk annotation line width with Aspose.PDF for .NET
type: docs
weight: 110
url: /pdf/net/annotations/lnkannotationlinewidth/
---
The example shows how to lnk annotation line width with Aspose.PDF for .NET


```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            doc.Pages.Add();
            IList<Point[]> inkList = new List<Point[]>();
            LineInfo lineInfo = new LineInfo();
            lineInfo.VerticeCoordinate = new float[] { 55, 55, 70, 70, 70, 90, 150, 60 };
            lineInfo.Visibility = true;
            lineInfo.LineColor = System.Drawing.Color.Red;
            lineInfo.LineWidth = 2;
            int length = lineInfo.VerticeCoordinate.Length / 2;
            Aspose.Pdf.Point[] gesture = new Aspose.Pdf.Point[length];
            for (int i = 0; i < length; i++)
            {
               gesture[i] = new Aspose.Pdf.Point(lineInfo.VerticeCoordinate[2 * i], lineInfo.VerticeCoordinate[2 * i + 1]);
            }

            inkList.Add(gesture);
            InkAnnotation a1 = new InkAnnotation(doc.Pages[1], new Aspose.Pdf.Rectangle(100, 100, 300, 300), inkList);
            a1.Subject = "Test";
            a1.Title = "Title";
            a1.Color = Aspose.Pdf.Color.FromRgb(System.Drawing.Color.Green);
            Border border = new Border(a1);
            border.Width = 3;
            border.Effect = BorderEffect.Cloudy;
            border.Dash = new Dash(1, 1);
            border.Style = BorderStyle.Solid;
            doc.Pages[1].Annotations.Add(a1);

            dataDir = dataDir + "lnkAnnotationLineWidth_out.pdf";
            // Save output file
            doc.Save(dataDir);

        
```


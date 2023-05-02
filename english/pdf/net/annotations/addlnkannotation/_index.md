---
title: Addlnk Annotation
linktitle: Addlnk Annotation
second_title: Aspose.PDF for .NET API Reference
description: The example shows how to addlnk annotation with Aspose.PDF for .NET
type: docs
weight: 20
url: /pdf/net/annotations/addlnkannotation/
---
The example shows how to addlnk annotation with Aspose.PDF for .NET


```csharp

            
            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir_AsposePdf_Annotations();

            Document doc = new Document();
            Page pdfPage = doc.Pages.Add();
            System.Drawing.Rectangle drect = new System.Drawing.Rectangle();
            drect.Height = (int)pdfPage.Rect.Height;
            drect.Width = (int)pdfPage.Rect.Width;
            drect.X = 0;
            drect.Y = 0;
            Aspose.Pdf.Rectangle arect = Aspose.Pdf.Rectangle.FromRect(drect);
            IList<Point[]> inkList = new List<Point[]>();
            Aspose.Pdf.Point[] arrpt = new Aspose.Pdf.Point[3];
            inkList.Add(arrpt);
            arrpt[0] = new Aspose.Pdf.Point(100, 800);
            arrpt[1] = new Aspose.Pdf.Point(200, 800);
            arrpt[2] = new Aspose.Pdf.Point(200, 700);
            InkAnnotation ia = new InkAnnotation(pdfPage, arect, inkList);
            ia.Title = "XXX";
            ia.Color = Aspose.Pdf.Color.LightBlue; // (GetColorFromString(stroke.InkColor));
            ia.CapStyle = CapStyle.Rounded;
            Border border = new Border(ia);
            border.Width = 25;
            ia.Opacity = 0.5;
            pdfPage.Annotations.Add(ia);

            dataDir = dataDir + "AddlnkAnnotation_out.pdf";
            // Save output file
            doc.Save(dataDir);
            
            Console.WriteLine("\nlnk annotation added successfully.\nFile saved at " + dataDir);
        
```

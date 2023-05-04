---
title: Set Callout Property
linktitle: Set Callout Property
second_title: Aspose.PDF for .NET API Reference
description: The example shows how to set callout property with Aspose.PDF for .NET
type: docs
weight: 130
url: /pdf/net/annotations/setcalloutproperty/
---
The example shows how to set callout property with Aspose.PDF for .NET


```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            Page page = doc.Pages.Add();
            DefaultAppearance da = new DefaultAppearance();
            da.TextColor = System.Drawing.Color.Red;
            da.FontSize = 10;
            FreeTextAnnotation fta = new FreeTextAnnotation(page, new Rectangle(422.25, 645.75, 583.5, 702.75), da);
            fta.Intent = FreeTextIntent.FreeTextCallout;
            fta.EndingStyle = LineEnding.OpenArrow;
            fta.Callout = new Point[]
            {
                new Point(428.25,651.75), new Point(462.75,681.375), new Point(474,681.375)
            };
            page.Annotations.Add(fta);
            fta.RichText = "<body xmlns=\"http://www.w3.org/1999/xhtml\" xmlns:xfa=\"http://www.xfa.org/schema/xfa-data/1.0/\" xfa:APIVersion=\"Acrobat:11.0.23\" xfa:spec=\"2.0.2\"  style=\"color:#FF0000;font-weight:normal;font-style:normal;font-stretch:normal\"><p dir=\"ltr\"><span style=\"font-size:9.0pt;font-family:Helvetica\">This is a sample</span></p></body>";
            doc.Save(dataDir + "SetCalloutProperty.pdf");

            
        
```


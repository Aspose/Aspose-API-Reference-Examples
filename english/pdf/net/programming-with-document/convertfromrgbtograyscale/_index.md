---
title: Convert From RGBTo Grayscale
linktitle: Convert From RGBTo Grayscale
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 60
url: /pdf/net/programming-with-document/convertfromrgbtograyscale/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Load source PDF file
            using (Document document = new Document(dataDir + "input.pdf"))
            {
                Aspose.Pdf.RgbToDeviceGrayConversionStrategy strategy = new Aspose.Pdf.RgbToDeviceGrayConversionStrategy();
                for (int idxPage = 1; idxPage <= document.Pages.Count; idxPage++)
                {
                    // Get instance of particular page inside PDF
                    Page page = document.Pages[idxPage];
                    // Convert the RGB colorspace image to GrayScale colorspace
                    strategy.Convert(page);
                }
                // Save resultant file
                document.Save(dataDir + "Test-gray_out.pdf");
            }
            
        
```


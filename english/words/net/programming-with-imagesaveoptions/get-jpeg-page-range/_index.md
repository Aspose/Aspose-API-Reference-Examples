---
title: Get Jpeg Page Range
linktitle: Get Jpeg Page Range
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-imagesaveoptions/get-jpeg-page-range/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

            // Set the "PageSet" to "0" to convert only the first page of a document.
            options.PageSet = new PageSet(0);

            // Change the image's brightness and contrast.
            // Both are on a 0-1 scale and are at 0.5 by default.
            options.ImageBrightness = 0.3f;
            options.ImageContrast = 0.7f;

            // Change the horizontal resolution.
            // The default value for these properties is 96.0, for a resolution of 96dpi.
            options.HorizontalResolution = 72f;

            doc.Save(ArtifactsDir + "WorkingWithImageSaveOptions.GetJpegPageRange.jpeg", options);
            
        
```


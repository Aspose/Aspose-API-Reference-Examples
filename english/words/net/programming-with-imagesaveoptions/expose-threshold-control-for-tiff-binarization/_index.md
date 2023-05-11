---
title: Expose Threshold Control For Tiff Binarization
linktitle: Expose Threshold Control For Tiff Binarization
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-imagesaveoptions/expose-threshold-control-for-tiff-binarization/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Tiff)
            {
                TiffCompression = TiffCompression.Ccitt3,
                ImageColorMode = ImageColorMode.Grayscale,
                TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
                ThresholdForFloydSteinbergDithering = 254
            };

            doc.Save(ArtifactsDir + "WorkingWithImageSaveOptions.ExposeThresholdControlForTiffBinarization.tiff", saveOptions);
            
        
```


---
title: Get Tiff Page Range
linktitle: Get Tiff Page Range
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-imagesaveoptions/get-tiff-page-range/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");
            
            doc.Save(ArtifactsDir + "WorkingWithImageSaveOptions.MultipageTiff.tiff");
            
            
            
            ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Tiff)
            {
                PageSet = new PageSet(new PageRange(0, 1)), TiffCompression = TiffCompression.Ccitt4, Resolution = 160
            };

            doc.Save(ArtifactsDir + "WorkingWithImageSaveOptions.GetTiffPageRange.tiff", saveOptions);
            
            
        
```


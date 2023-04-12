---
title: Programming With Imagesaveoptions
linktitle: Programming With Imagesaveoptions
second_title: Aspose.Words for .NET API Reference
description: Examples contain expose threshold control for tiff binarization, get tiff page range, format 1bpp indexed, get jpeg page range and page saving callback
type: docs
weight: 1630
url: /words/net/programming-with-imagesaveoptions/
---
Examples contain expose threshold control for tiff binarization, get tiff page range, format 1bpp indexed, get jpeg page range and page saving callback

## Expose Threshold Control For Tiff Binarization

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

## Get Tiff Page Range

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");
            
            doc.Save(ArtifactsDir + "WorkingWithImageSaveOptions.MultipageTiff.tiff");
            
            
            
            ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Tiff)
            {
                PageSet = new PageSet(new PageRange(0, 1)), TiffCompression = TiffCompression.Ccitt4, Resolution = 160
            };

            doc.Save(ArtifactsDir + "WorkingWithImageSaveOptions.GetTiffPageRange.tiff", saveOptions);
            
            
        
```

## Format 1Bpp Indexed

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png)
            {
                PageSet = new PageSet(1),
                ImageColorMode = ImageColorMode.BlackAndWhite,
                PixelFormat = ImagePixelFormat.Format1bppIndexed
            };

            doc.Save(ArtifactsDir + "WorkingWithImageSaveOptions.Format1BppIndexed.Png", saveOptions);
            
        
```

## Get Jpeg Page Range

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

## Page Saving Callback

```csharp

            Document doc = new Document(MyDir + "Rendering.docx");

            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png)
            {
                PageSet = new PageSet(new PageRange(0, doc.PageCount - 1)),
                PageSavingCallback = new HandlePageSavingCallback()
            };

            doc.Save(ArtifactsDir + "WorkingWithImageSaveOptions.PageSavingCallback.png", imageSaveOptions);
        
```


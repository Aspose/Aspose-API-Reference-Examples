---
title: Downsampling Images
linktitle: Downsampling Images
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/downsampling-images/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            // We can set a minimum threshold for downsampling.
            // This value will prevent the second image in the input document from being downsampled.
            PdfSaveOptions saveOptions = new PdfSaveOptions
            {
                DownsampleOptions = { Resolution = 36, ResolutionThreshold = 128 }
            };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.DownsamplingImages.pdf", saveOptions);
            
        
```


---
title: Image Compression
linktitle: Image Compression
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/image-compression/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions
            {
                ImageCompression = PdfImageCompression.Jpeg, PreserveFormFields = true
            };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.PdfImageCompression.pdf", saveOptions);

            PdfSaveOptions saveOptionsA2U = new PdfSaveOptions
            {
                Compliance = PdfCompliance.PdfA2u,
                ImageCompression = PdfImageCompression.Jpeg,
                JpegQuality = 100, // Use JPEG compression at 50% quality to reduce file size.
            };

            

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.PdfImageCompression_A2u.pdf", saveOptionsA2U);
            
        
```


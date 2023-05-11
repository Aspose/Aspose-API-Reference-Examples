---
title: Interpolate Images
linktitle: Interpolate Images
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/interpolate-images/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions { InterpolateImages = true };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.InterpolateImages.pdf", saveOptions);
            
        
```


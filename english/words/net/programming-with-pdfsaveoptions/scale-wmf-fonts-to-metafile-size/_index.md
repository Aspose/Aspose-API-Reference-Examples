---
title: Scale Wmf Fonts To Metafile Size
linktitle: Scale Wmf Fonts To Metafile Size
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/scale-wmf-fonts-to-metafile-size/
---




```csharp

            
            Document doc = new Document(MyDir + "WMF with text.docx");

            MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions
            {
                ScaleWmfFontsToMetafileSize = false
            };

            // If Aspose.Words cannot correctly render some of the metafile records to vector graphics
            // then Aspose.Words renders this metafile to a bitmap.
            PdfSaveOptions saveOptions = new PdfSaveOptions { MetafileRenderingOptions = metafileRenderingOptions };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.ScaleWmfFontsToMetafileSize.pdf", saveOptions);
            
        
```


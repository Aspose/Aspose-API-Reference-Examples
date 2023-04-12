---
title: Programming With Pclsaveoptions
linktitle: Programming With Pclsaveoptions
second_title: Aspose.Words for .NET API Reference
description: Examples contain rasterize transformed elements
type: docs
weight: 1670
url: /words/net/programming-with-pclsaveoptions/
---
Examples contain rasterize transformed elements

## Rasterize Transformed Elements

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PclSaveOptions saveOptions = new PclSaveOptions
            {
                SaveFormat = SaveFormat.Pcl, RasterizeTransformedElements = false
            };

            doc.Save(ArtifactsDir + "WorkingWithPclSaveOptions.RasterizeTransformedElements.pcl", saveOptions);
            
        
```


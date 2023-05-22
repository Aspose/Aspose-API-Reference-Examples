---
title: Rasterize Transformed Elements
linktitle: Rasterize Transformed Elements
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pclsaveoptions/rasterize-transformed-elements/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PclSaveOptions saveOptions = new PclSaveOptions
            {
                SaveFormat = SaveFormat.Pcl, RasterizeTransformedElements = false
            };

            doc.Save(ArtifactsDir + "WorkingWithPclSaveOptions.RasterizeTransformedElements.pcl", saveOptions);
            
        
```


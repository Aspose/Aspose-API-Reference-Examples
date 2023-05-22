---
title: Dml 3DEffects Rendering
linktitle: Dml 3DEffects Rendering
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/dml-3deffects-rendering/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions { Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.Dml3DEffectsRendering.pdf", saveOptions);
            
        
```


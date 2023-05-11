---
title: Disable Embed Windows Fonts
linktitle: Disable Embed Windows Fonts
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/disable-embed-windows-fonts/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            // The output PDF will be saved without embedding standard windows fonts.
            PdfSaveOptions saveOptions = new PdfSaveOptions { FontEmbeddingMode = PdfFontEmbeddingMode.EmbedNone };
            
            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.DisableEmbedWindowsFonts.pdf", saveOptions);
            
        
```


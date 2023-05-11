---
title: Embedded Subset Fonts
linktitle: Embedded Subset Fonts
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/embedded-subset-fonts/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            // The output PDF will contain subsets of the fonts in the document.
            // Only the glyphs used in the document are included in the PDF fonts.
            PdfSaveOptions saveOptions = new PdfSaveOptions { EmbedFullFonts = false };
            
            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.EmbeddSubsetFonts.pdf", saveOptions);
            
        
```


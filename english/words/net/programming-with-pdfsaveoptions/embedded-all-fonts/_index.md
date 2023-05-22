---
title: Embedded All Fonts
linktitle: Embedded All Fonts
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/embedded-all-fonts/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            // The output PDF will be embedded with all fonts found in the document.
            PdfSaveOptions saveOptions = new PdfSaveOptions { EmbedFullFonts = true };
            
            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.EmbeddedFontsInPdf.pdf", saveOptions);
            
        
```


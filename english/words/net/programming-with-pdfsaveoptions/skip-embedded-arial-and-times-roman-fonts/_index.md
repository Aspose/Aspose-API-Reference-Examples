---
title: Skip Embedded Arial And Times Roman Fonts
linktitle: Skip Embedded Arial And Times Roman Fonts
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/skip-embedded-arial-and-times-roman-fonts/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions { FontEmbeddingMode = PdfFontEmbeddingMode.EmbedAll };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.SkipEmbeddedArialAndTimesRomanFonts.pdf", saveOptions);
            
        
```


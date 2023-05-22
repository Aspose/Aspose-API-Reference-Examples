---
title: Avoid Embedding Core Fonts
linktitle: Avoid Embedding Core Fonts
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/avoid-embedding-core-fonts/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            // The output PDF will not be embedded with core fonts such as Arial, Times New Roman etc.
            PdfSaveOptions saveOptions = new PdfSaveOptions { UseCoreFonts = true };
            
            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.AvoidEmbeddingCoreFonts.pdf", saveOptions);
            
        
```


---
title: Additional Text Positioning
linktitle: Additional Text Positioning
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/additional-text-positioning/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions { AdditionalTextPositioning = true };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
            
        
```


---
title: Display Doc Title In Window Titlebar
linktitle: Display Doc Title In Window Titlebar
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/display-doc-title-in-window-titlebar/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions { DisplayDocTitle = true };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.DisplayDocTitleInWindowTitlebar.pdf", saveOptions);
            
        
```


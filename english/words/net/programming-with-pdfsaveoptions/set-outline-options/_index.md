---
title: Set Outline Options
linktitle: Set Outline Options
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/set-outline-options/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions();
            saveOptions.OutlineOptions.HeadingsOutlineLevels = 3;
            saveOptions.OutlineOptions.ExpandedOutlineLevels = 1;

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.SetOutlineOptions.pdf", saveOptions);
            
        
```


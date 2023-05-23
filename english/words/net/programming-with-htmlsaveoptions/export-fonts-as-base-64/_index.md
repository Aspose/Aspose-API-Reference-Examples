---
title: Export Fonts As Base 64
linktitle: Export Fonts As Base 64
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-htmlsaveoptions/export-fonts-as-base-64/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            HtmlSaveOptions saveOptions = new HtmlSaveOptions { ExportFontsAsBase64 = true };

            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.ExportFontsAsBase64.html", saveOptions);
            
        
```


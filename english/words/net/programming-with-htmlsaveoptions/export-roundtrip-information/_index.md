---
title: Export Roundtrip Information
linktitle: Export Roundtrip Information
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-htmlsaveoptions/export-roundtrip-information/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            HtmlSaveOptions saveOptions = new HtmlSaveOptions { ExportRoundtripInformation = true };

            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.ExportRoundtripInformation.html", saveOptions);
            
        
```


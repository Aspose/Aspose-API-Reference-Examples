---
title: Export Cid Urls For Mhtml Resources
linktitle: Export Cid Urls For Mhtml Resources
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-htmlsaveoptions/export-cid-urls-for-mhtml-resources/
---




```csharp

            
            Document doc = new Document(MyDir + "Content-ID.docx");

            HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Mhtml)
            {
                PrettyFormat = true, ExportCidUrlsForMhtmlResources = true
            };

            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.ExportCidUrlsForMhtmlResources.mhtml", saveOptions);
            
        
```


---
title: Export Resources
linktitle: Export Resources
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-htmlsaveoptions/export-resources/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            HtmlSaveOptions saveOptions = new HtmlSaveOptions
            {
                CssStyleSheetType = CssStyleSheetType.External,
                ExportFontResources = true,
                ResourceFolder = ArtifactsDir + "Resources",
                ResourceFolderAlias = "http://example.com/resources"
            };

            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.ExportResources.html", saveOptions);
            
        
```


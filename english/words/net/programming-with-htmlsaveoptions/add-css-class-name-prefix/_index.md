---
title: Add Css Class Name Prefix
linktitle: Add Css Class Name Prefix
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-htmlsaveoptions/add-css-class-name-prefix/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            HtmlSaveOptions saveOptions = new HtmlSaveOptions
            {
                CssStyleSheetType = CssStyleSheetType.External, CssClassNamePrefix = "pfx_"
            };
            
            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.AddCssClassNamePrefix.html", saveOptions);
            
        
```


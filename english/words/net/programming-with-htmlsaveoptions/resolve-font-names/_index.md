---
title: Resolve Font Names
linktitle: Resolve Font Names
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-htmlsaveoptions/resolve-font-names/
---




```csharp

            
            Document doc = new Document(MyDir + "Missing font.docx");

            HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html)
            {
                PrettyFormat = true, ResolveFontNames = true
            };

            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.ResolveFontNames.html", saveOptions);
            
        
```


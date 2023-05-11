---
title: Convert Metafiles To Emf Or Wmf
linktitle: Convert Metafiles To Emf Or Wmf
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-htmlsaveoptions/convert-metafiles-to-emf-or-wmf/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Write("Here is an image as is: ");
            builder.InsertHtml(
                @"<img src=""data:image/png;base64,
                    iVBORw0KGgoAAAANSUhEUgAAAAoAAAAKCAYAAACNMs+9AAAABGdBTUEAALGP
                    C/xhBQAAAAlwSFlzAAALEwAACxMBAJqcGAAAAAd0SU1FB9YGARc5KB0XV+IA
                    AAAddEVYdENvbW1lbnQAQ3JlYXRlZCB3aXRoIFRoZSBHSU1Q72QlbgAAAF1J
                    REFUGNO9zL0NglAAxPEfdLTs4BZM4DIO4C7OwQg2JoQ9LE1exdlYvBBeZ7jq
                    ch9//q1uH4TLzw4d6+ErXMMcXuHWxId3KOETnnXXV6MJpcq2MLaI97CER3N0
                    vr4MkhoXe0rZigAAAABJRU5ErkJggg=="" alt=""Red dot"" />");

            HtmlSaveOptions saveOptions = new HtmlSaveOptions { MetafileFormat = HtmlMetafileFormat.EmfOrWmf };

            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.ConvertMetafilesToEmfOrWmf.html", saveOptions);
            
        
```


---
title: Programming With Htmlsaveoptions
linktitle: Programming With Htmlsaveoptions
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain export roundtrip information, export fonts as base 64, export resources, convert metafiles to emf or wmf, convert metafiles to svg, add css cla
type: docs
weight: 1620
url: /words/net/programming-with-htmlsaveoptions/
---
Tutorials contain export roundtrip information, export fonts as base 64, export resources, convert metafiles to emf or wmf, convert metafiles to svg, add css class name prefix, export cid urls for mhtml resources, resolve font names and export text input form field as text

## Export Roundtrip Information

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            HtmlSaveOptions saveOptions = new HtmlSaveOptions { ExportRoundtripInformation = true };

            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.ExportRoundtripInformation.html", saveOptions);
            
        
```

## Export Fonts As Base 64

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            HtmlSaveOptions saveOptions = new HtmlSaveOptions { ExportFontsAsBase64 = true };

            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.ExportFontsAsBase64.html", saveOptions);
            
        
```

## Export Resources

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

## Convert Metafiles To Emf Or Wmf

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

## Convert Metafiles To Svg

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.Write("Here is an SVG image: ");
            builder.InsertHtml(
                @"<svg height='210' width='500'>
                <polygon points='100,10 40,198 190,78 10,78 160,198' 
                    style='fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;' />
            </svg> ");

            HtmlSaveOptions saveOptions = new HtmlSaveOptions { MetafileFormat = HtmlMetafileFormat.Svg };

            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.ConvertMetafilesToSvg.html", saveOptions);
            
        
```

## Add Css Class Name Prefix

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            HtmlSaveOptions saveOptions = new HtmlSaveOptions
            {
                CssStyleSheetType = CssStyleSheetType.External, CssClassNamePrefix = "pfx_"
            };
            
            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.AddCssClassNamePrefix.html", saveOptions);
            
        
```

## Export Cid Urls For Mhtml Resources

```csharp

            
            Document doc = new Document(MyDir + "Content-ID.docx");

            HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Mhtml)
            {
                PrettyFormat = true, ExportCidUrlsForMhtmlResources = true
            };

            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.ExportCidUrlsForMhtmlResources.mhtml", saveOptions);
            
        
```

## Resolve Font Names

```csharp

            
            Document doc = new Document(MyDir + "Missing font.docx");

            HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html)
            {
                PrettyFormat = true, ResolveFontNames = true
            };

            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.ResolveFontNames.html", saveOptions);
            
        
```

## Export Text Input Form Field As Text

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            string imagesDir = Path.Combine(ArtifactsDir, "Images");

            // The folder specified needs to exist and should be empty.
            if (Directory.Exists(imagesDir))
                Directory.Delete(imagesDir, true);

            Directory.CreateDirectory(imagesDir);

            // Set an option to export form fields as plain text, not as HTML input elements.
            HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html)
            {
                ExportTextInputFormFieldAsText = true, ImagesFolder = imagesDir
            };

            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.ExportTextInputFormFieldAsText.html", saveOptions);
            
        
```


---
title: Programming With Htmlfixedsaveoptions
linktitle: Programming With Htmlfixedsaveoptions
second_title: Aspose.Words for .NET API Reference
description: Examples contain use font from target machine and write all css rules in single file
type: docs
weight: 1610
url: /words/net/programming-with-htmlfixedsaveoptions/
---
Examples contain use font from target machine and write all css rules in single file

## Use Font From Target Machine

```csharp

            
            Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

            HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { UseTargetMachineFonts = true };

            doc.Save(ArtifactsDir + "WorkingWithHtmlFixedSaveOptions.UseFontFromTargetMachine.html", saveOptions);
            
        
```

## Write All Css Rules In Single File

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            // Setting this property to true restores the old behavior (separate files) for compatibility with legacy code.
            // All CSS rules are written into single file "styles.css.
            HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { SaveFontFaceCssSeparately = false };
            
            doc.Save(ArtifactsDir + "WorkingWithHtmlFixedSaveOptions.WriteAllCssRulesInSingleFile.html", saveOptions);
            
        
```


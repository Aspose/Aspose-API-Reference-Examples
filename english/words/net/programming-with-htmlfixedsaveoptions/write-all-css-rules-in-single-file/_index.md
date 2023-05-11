---
title: Write All Css Rules In Single File
linktitle: Write All Css Rules In Single File
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-htmlfixedsaveoptions/write-all-css-rules-in-single-file/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            // Setting this property to true restores the old behavior (separate files) for compatibility with legacy code.
            // All CSS rules are written into single file "styles.css.
            HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { SaveFontFaceCssSeparately = false };
            
            doc.Save(ArtifactsDir + "WorkingWithHtmlFixedSaveOptions.WriteAllCssRulesInSingleFile.html", saveOptions);
            
        
```


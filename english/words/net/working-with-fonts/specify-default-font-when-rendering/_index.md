---
title: Specify Default Font When Rendering
linktitle: Specify Default Font When Rendering
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/specify-default-font-when-rendering/
---




```csharp
            
            Document doc = new Document(MyDir + "Rendering.docx");

            FontSettings fontSettings = new FontSettings();
            // If the default font defined here cannot be found during rendering then
            // the closest font on the machine is used instead.
            fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial Unicode MS";
            
            doc.FontSettings = fontSettings;
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.SpecifyDefaultFontWhenRendering.pdf");
            
```


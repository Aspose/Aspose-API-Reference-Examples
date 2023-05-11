---
title: Set True Type Fonts Folder
linktitle: Set True Type Fonts Folder
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/set-true-type-fonts-folder/
---




```csharp
            
            Document doc = new Document(MyDir + "Rendering.docx");

            FontSettings fontSettings = new FontSettings();
            // Note that this setting will override any default font sources that are being searched by default. Now only these folders will be searched for
            // Fonts when rendering or embedding fonts. To add an extra font source while keeping system font sources then use both FontSettings.GetFontSources and
            // FontSettings.SetFontSources instead
            fontSettings.SetFontsFolder(@"C:\MyFonts\", false);
            // Set font settings
            doc.FontSettings = fontSettings;
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.SetTrueTypeFontsFolder.pdf");
            
```


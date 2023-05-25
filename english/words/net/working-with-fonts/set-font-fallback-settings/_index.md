---
title: Set Font Fallback Settings
linktitle: Set Font Fallback Settings
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/set-font-fallback-settings/
---
### Sample source code for Set Font Fallback Settings using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Rendering.docx");
            FontSettings fontSettings = new FontSettings();
            fontSettings.FallbackSettings.Load(dataDir + "Font fallback rules.xml");
            doc.FontSettings = fontSettings;
            doc.Save(dataDir + "WorkingWithFonts.SetFontFallbackSettings.pdf");
```
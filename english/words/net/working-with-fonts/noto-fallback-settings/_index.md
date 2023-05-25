---
title: Noto Fallback Settings
linktitle: Noto Fallback Settings
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/noto-fallback-settings/
---
### Sample source code for Noto Fallback Settings using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Rendering.docx");
            FontSettings fontSettings = new FontSettings();
            fontSettings.FallbackSettings.LoadNotoFallbackSettings();
            doc.FontSettings = fontSettings;
            doc.Save(dataDir + "WorkingWithFonts.NotoFallbackSettings.pdf");
```
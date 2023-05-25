---
title: Enable Disable Font Substitution
linktitle: Enable Disable Font Substitution
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/enable-disable-font-substitution/
---
### Sample source code for Enable Disable Font Substitution using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Rendering.docx");
            FontSettings fontSettings = new FontSettings();
            fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
            fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = false;
            doc.FontSettings = fontSettings;
            doc.Save(dataDir + "WorkingWithFonts.EnableDisableFontSubstitution.pdf");
```
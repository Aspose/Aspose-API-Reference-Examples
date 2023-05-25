---
title: Set Fonts Folder
linktitle: Set Fonts Folder
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/set-fonts-folder/
---
### Sample source code for Set Fonts Folder using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            FontSettings fontSettings = new FontSettings();
            fontSettings.SetFontsFolder(dataDir + "Fonts", false);
            LoadOptions loadOptions = new LoadOptions();
            loadOptions.FontSettings = fontSettings;
            Document doc = new Document(dataDir + "Rendering.docx", loadOptions);
```
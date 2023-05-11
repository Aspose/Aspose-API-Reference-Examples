---
title: Set Fonts Folder
linktitle: Set Fonts Folder
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/set-fonts-folder/
---




```csharp
            
            FontSettings fontSettings = new FontSettings();
            fontSettings.SetFontsFolder(MyDir + "Fonts", false);
            
            LoadOptions loadOptions = new LoadOptions();
            loadOptions.FontSettings = fontSettings;
            
            Document doc = new Document(MyDir + "Rendering.docx", loadOptions);
            
```


---
title: Font Settings Default Instance
linktitle: Font Settings Default Instance
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/font-settings-default-instance/
---




```csharp
            
            
            FontSettings fontSettings = FontSettings.DefaultInstance;
            
            fontSettings.SetFontsSources(new FontSourceBase[]
            {
                new SystemFontSource(),
                new FolderFontSource("C:\\MyFonts\\", true)
            });
            

            LoadOptions loadOptions = new LoadOptions();
            loadOptions.FontSettings = fontSettings;
            Document doc = new Document(MyDir + "Rendering.docx", loadOptions);
```


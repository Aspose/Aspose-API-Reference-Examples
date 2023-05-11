---
title: Set Fonts Folders
linktitle: Set Fonts Folders
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/set-fonts-folders/
---




```csharp
            
            FontSettings.DefaultInstance.SetFontsSources(new FontSourceBase[]
            {
                new SystemFontSource(), new FolderFontSource("C:\\MyFonts\\", true)
            });

            Document doc = new Document(MyDir + "Rendering.docx");
            doc.Save(ArtifactsDir + "WorkingWithFonts.SetFontsFolders.pdf");
            
```


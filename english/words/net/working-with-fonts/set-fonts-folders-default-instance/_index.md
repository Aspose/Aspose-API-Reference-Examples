---
title: Set Fonts Folders Default Instance
linktitle: Set Fonts Folders Default Instance
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/set-fonts-folders-default-instance/
---




```csharp
            
            FontSettings.DefaultInstance.SetFontsFolder("C:\\MyFonts\\", true);
            

            Document doc = new Document(MyDir + "Rendering.docx");
            doc.Save(ArtifactsDir + "WorkingWithFonts.SetFontsFoldersDefaultInstance.pdf");
```


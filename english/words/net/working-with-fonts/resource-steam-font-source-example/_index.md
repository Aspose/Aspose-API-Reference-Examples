---
title: Resource Steam Font Source Example
linktitle: Resource Steam Font Source Example
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/resource-steam-font-source-example/
---




```csharp
            Document doc = new Document(MyDir + "Rendering.docx");
            
            FontSettings.DefaultInstance.SetFontsSources(new FontSourceBase[]
                { new SystemFontSource(), new ResourceSteamFontSource() });

            doc.Save(ArtifactsDir + "WorkingWithFonts.SetFontsFolders.pdf");
```


---
title: Noto Fallback Settings
linktitle: Noto Fallback Settings
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/noto-fallback-settings/
---




```csharp
            
            Document doc = new Document(MyDir + "Rendering.docx");

            FontSettings fontSettings = new FontSettings();
            fontSettings.FallbackSettings.LoadNotoFallbackSettings();
            
            doc.FontSettings = fontSettings;
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.NotoFallbackSettings.pdf");
            
```


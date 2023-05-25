---
title: Resource Steam Font Source Example
linktitle: Resource Steam Font Source Example
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/resource-steam-font-source-example/
---
### Sample source code for Resource Steam Font Source Example using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Rendering.docx");
            FontSettings.DefaultInstance.SetFontsSources(new FontSourceBase[]
                { new SystemFontSource(), new ResourceSteamFontSource() });
            doc.Save(dataDir + "WorkingWithFonts.SetFontsFolders.pdf");
```
---
title: Set Fonts Folders
linktitle: Set Fonts Folders
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/set-fonts-folders/
---
### Sample source code for Set Fonts Folders using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            FontSettings.DefaultInstance.SetFontsSources(new FontSourceBase[]
            {
                new SystemFontSource(), new FolderFontSource("C:\\MyFonts\\", true)
            });
            Document doc = new Document(dataDir + "Rendering.docx");
            doc.Save(dataDir + "WorkingWithFonts.SetFontsFolders.pdf");
```
---
title: Set Fonts Folders Default Instance
linktitle: Set Fonts Folders Default Instance
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/set-fonts-folders-default-instance/
---
### Sample source code for Set Fonts Folders Default Instance using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            FontSettings.DefaultInstance.SetFontsFolder("C:\\MyFonts\\", true);
            Document doc = new Document(dataDir + "Rendering.docx");
            doc.Save(dataDir + "WorkingWithFonts.SetFontsFoldersDefaultInstance.pdf");
```
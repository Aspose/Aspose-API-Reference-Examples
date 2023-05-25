---
title: Get List Of Available Fonts
linktitle: Get List Of Available Fonts
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/get-list-of-available-fonts/
---
### Sample source code for Get List Of Available Fonts using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            FontSettings fontSettings = new FontSettings();
            List<FontSourceBase> fontSources = new List<FontSourceBase>(fontSettings.GetFontsSources());
            // Add a new folder source which will instruct Aspose.Words to search the following folder for fonts.
            FolderFontSource folderFontSource = new FolderFontSource(dataDir, true);
            // Add the custom folder which contains our fonts to the list of existing font sources.
            fontSources.Add(folderFontSource);
            FontSourceBase[] updatedFontSources = fontSources.ToArray();
            foreach (PhysicalFontInfo fontInfo in updatedFontSources[0].GetAvailableFonts())
            {
                Console.WriteLine("FontFamilyName : " + fontInfo.FontFamilyName);
                Console.WriteLine("FullFontName  : " + fontInfo.FullFontName);
                Console.WriteLine("Version  : " + fontInfo.Version);
                Console.WriteLine("FilePath : " + fontInfo.FilePath);
            }
```
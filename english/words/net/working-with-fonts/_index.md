---
title: Working with Fonts
linktitle: Working with Fonts
second_title: Aspose.Words for .NET API Reference
description: Examples show how to apply font formatting, font line spacing, DMLText Effect, enable/disable font substitute, font fallback settings, get list of available font in Word Document using Aspose.Words for .NET
type: docs
weight: 420
url: /words/net/working-with-fonts/
---
The following examples show how to apply font formatting, font line spacing, DMLText Effect, enable/disable font substitute, font fallback settings, get list of available font in Word Document using Aspose.Words for .NET.

## Font Formatting

```csharp
            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Font font = builder.Font;
            font.Size = 16;
            font.Bold = true;
            font.Color = Color.Blue;
            font.Name = "Arial";
            font.Underline = Underline.Dash;

            builder.Write("Sample text.");
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.FontFormatting.docx");
            
```

## Get Font Line Spacing

```csharp
            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.Font.Name = "Calibri";
            builder.Writeln("qText");

            Font font = builder.Document.FirstSection.Body.FirstParagraph.Runs[0].Font;
            Console.WriteLine($"lineSpacing = {font.LineSpacing}");
            
```

## Check DMLText Effect

```csharp
            
            Document doc = new Document(MyDir + "DrawingML text effects.docx");
            
            RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
            Font runFont = runs[0].Font;

            // One run might have several Dml text effects applied.
            Console.WriteLine(runFont.HasDmlEffect(TextDmlEffect.Shadow));
            Console.WriteLine(runFont.HasDmlEffect(TextDmlEffect.Effect3D));
            Console.WriteLine(runFont.HasDmlEffect(TextDmlEffect.Reflection));
            Console.WriteLine(runFont.HasDmlEffect(TextDmlEffect.Outline));
            Console.WriteLine(runFont.HasDmlEffect(TextDmlEffect.Fill));
            
```

## Set Font Formatting

```csharp
            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Font font = builder.Font;
            font.Bold = true;
            font.Color = Color.DarkBlue;
            font.Italic = true;
            font.Name = "Arial";
            font.Size = 24;
            font.Spacing = 5;
            font.Underline = Underline.Double;

            builder.Writeln("I'm a very nice formatted string.");
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.SetFontFormatting.docx");
            
```

## Set Font Emphasis Mark

```csharp
            
            Document document = new Document();
            DocumentBuilder builder = new DocumentBuilder(document);

            builder.Font.EmphasisMark = EmphasisMark.UnderSolidCircle;

            builder.Write("Emphasis text");
            builder.Writeln();
            builder.Font.ClearFormatting();
            builder.Write("Simple text");

            document.Save(ArtifactsDir + "WorkingWithFonts.SetFontEmphasisMark.docx");
            
```

## Set Fonts Folders

```csharp
            
            FontSettings.DefaultInstance.SetFontsSources(new FontSourceBase[]
            {
                new SystemFontSource(), new FolderFontSource("C:\\MyFonts\\", true)
            });

            Document doc = new Document(MyDir + "Rendering.docx");
            doc.Save(ArtifactsDir + "WorkingWithFonts.SetFontsFolders.pdf");
            
```

## Enable Disable Font Substitution

```csharp
            
            Document doc = new Document(MyDir + "Rendering.docx");

            FontSettings fontSettings = new FontSettings();
            fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
            fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = false;
            
            doc.FontSettings = fontSettings;
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.EnableDisableFontSubstitution.pdf");
            
```

## Set Font Fallback Settings

```csharp
            
            Document doc = new Document(MyDir + "Rendering.docx");

            FontSettings fontSettings = new FontSettings();
            fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");
            
            doc.FontSettings = fontSettings;
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.SetFontFallbackSettings.pdf");
            
```

## Noto Fallback Settings

```csharp
            
            Document doc = new Document(MyDir + "Rendering.docx");

            FontSettings fontSettings = new FontSettings();
            fontSettings.FallbackSettings.LoadNotoFallbackSettings();
            
            doc.FontSettings = fontSettings;
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.NotoFallbackSettings.pdf");
            
```

## Set Fonts Folders Default Instance

```csharp
            
            FontSettings.DefaultInstance.SetFontsFolder("C:\\MyFonts\\", true);
            

            Document doc = new Document(MyDir + "Rendering.docx");
            doc.Save(ArtifactsDir + "WorkingWithFonts.SetFontsFoldersDefaultInstance.pdf");
```

## Set Fonts Folders Multiple Folders

```csharp
            
            Document doc = new Document(MyDir + "Rendering.docx");
            
            FontSettings fontSettings = new FontSettings();
            // Note that this setting will override any default font sources that are being searched by default. Now only these folders will be searched for
            // fonts when rendering or embedding fonts. To add an extra font source while keeping system font sources then use both FontSettings.GetFontSources and
            // FontSettings.SetFontSources instead.
            fontSettings.SetFontsFolders(new[] { @"C:\MyFonts\", @"D:\Misc\Fonts\" }, true);
            
            doc.FontSettings = fontSettings;
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.SetFontsFoldersMultipleFolders.pdf");
            
```

## Set Fonts Folders System And Custom Folder

```csharp
            
            Document doc = new Document(MyDir + "Rendering.docx");
            
            FontSettings fontSettings = new FontSettings();
            // Retrieve the array of environment-dependent font sources that are searched by default.
            // For example this will contain a "Windows\Fonts\" source on a Windows machines.
            // We add this array to a new List to make adding or removing font entries much easier.
            List<FontSourceBase> fontSources = new List<FontSourceBase>(fontSettings.GetFontsSources());

            // Add a new folder source which will instruct Aspose.Words to search the following folder for fonts.
            FolderFontSource folderFontSource = new FolderFontSource("C:\\MyFonts\\", true);

            // Add the custom folder which contains our fonts to the list of existing font sources.
            fontSources.Add(folderFontSource);

            FontSourceBase[] updatedFontSources = fontSources.ToArray();
            fontSettings.SetFontsSources(updatedFontSources);
            
            doc.FontSettings = fontSettings;
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.SetFontsFoldersSystemAndCustomFolder.pdf");
            
```

## Set Fonts Folders With Priority

```csharp
            
            FontSettings.DefaultInstance.SetFontsSources(new FontSourceBase[]
            {
                new SystemFontSource(), new FolderFontSource("C:\\MyFonts\\", true,1)
            });
            

            Document doc = new Document(MyDir + "Rendering.docx");
            doc.Save(ArtifactsDir + "WorkingWithFonts.SetFontsFoldersWithPriority.pdf");
```

## Set True Type Fonts Folder

```csharp
            
            Document doc = new Document(MyDir + "Rendering.docx");

            FontSettings fontSettings = new FontSettings();
            // Note that this setting will override any default font sources that are being searched by default. Now only these folders will be searched for
            // Fonts when rendering or embedding fonts. To add an extra font source while keeping system font sources then use both FontSettings.GetFontSources and
            // FontSettings.SetFontSources instead
            fontSettings.SetFontsFolder(@"C:\MyFonts\", false);
            // Set font settings
            doc.FontSettings = fontSettings;
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.SetTrueTypeFontsFolder.pdf");
            
```

## Specify Default Font When Rendering

```csharp
            
            Document doc = new Document(MyDir + "Rendering.docx");

            FontSettings fontSettings = new FontSettings();
            // If the default font defined here cannot be found during rendering then
            // the closest font on the machine is used instead.
            fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial Unicode MS";
            
            doc.FontSettings = fontSettings;
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.SpecifyDefaultFontWhenRendering.pdf");
            
```

## Font Settings With Load Options

```csharp
            
            FontSettings fontSettings = new FontSettings();

            TableSubstitutionRule substitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
            // If "UnknownFont1" font family is not available then substitute it by "Comic Sans MS"
            substitutionRule.AddSubstitutes("UnknownFont1", new string[] { "Comic Sans MS" });
            
            LoadOptions loadOptions = new LoadOptions();
            loadOptions.FontSettings = fontSettings;
            
            Document doc = new Document(MyDir + "Rendering.docx", loadOptions);
            
```

## Set Fonts Folder

```csharp
            
            FontSettings fontSettings = new FontSettings();
            fontSettings.SetFontsFolder(MyDir + "Fonts", false);
            
            LoadOptions loadOptions = new LoadOptions();
            loadOptions.FontSettings = fontSettings;
            
            Document doc = new Document(MyDir + "Rendering.docx", loadOptions);
            
```

## Font Settings With Load Option

```csharp
            
            LoadOptions loadOptions = new LoadOptions();
            loadOptions.FontSettings = new FontSettings();

            Document doc = new Document(MyDir + "Rendering.docx", loadOptions);
            
```

## Font Settings Default Instance

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

## Get List Of Available Fonts

```csharp
            
            FontSettings fontSettings = new FontSettings();
            List<FontSourceBase> fontSources = new List<FontSourceBase>(fontSettings.GetFontsSources());

            // Add a new folder source which will instruct Aspose.Words to search the following folder for fonts.
            FolderFontSource folderFontSource = new FolderFontSource(MyDir, true);
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

## Receive Notifications Of Fonts

```csharp
            
            Document doc = new Document(MyDir + "Rendering.docx");

            FontSettings fontSettings = new FontSettings();

            // We can choose the default font to use in the case of any missing fonts.
            fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
            // For testing we will set Aspose.Words to look for fonts only in a folder which doesn't exist. Since Aspose.Words won't
            // find any fonts in the specified directory, then during rendering the fonts in the document will be subsuited with the default
            // font specified under FontSettings.DefaultFontName. We can pick up on this subsuition using our callback.
            fontSettings.SetFontsFolder(string.Empty, false);

            // Create a new class implementing IWarningCallback which collect any warnings produced during document save.
            HandleDocumentWarnings callback = new HandleDocumentWarnings();

            doc.WarningCallback = callback;
            doc.FontSettings = fontSettings;
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.ReceiveNotificationsOfFonts.pdf");
            
```

## Receive Warning Notification

```csharp
            
            Document doc = new Document(MyDir + "Rendering.docx");
            
            // When you call UpdatePageLayout the document is rendered in memory. Any warnings that occured during rendering
            // are stored until the document save and then sent to the appropriate WarningCallback.
            doc.UpdatePageLayout();

            HandleDocumentWarnings callback = new HandleDocumentWarnings();
            doc.WarningCallback = callback;
            
            // Even though the document was rendered previously, any save warnings are notified to the user during document save.
            doc.Save(ArtifactsDir + "WorkingWithFonts.ReceiveWarningNotification.pdf");
            
```

## Resource Steam Font Source Example

```csharp
            Document doc = new Document(MyDir + "Rendering.docx");
            
            FontSettings.DefaultInstance.SetFontsSources(new FontSourceBase[]
                { new SystemFontSource(), new ResourceSteamFontSource() });

            doc.Save(ArtifactsDir + "WorkingWithFonts.SetFontsFolders.pdf");
```

## Get Substitution Without Suffixes

```csharp
            Document doc = new Document(MyDir + "Get substitution without suffixes.docx");

            DocumentSubstitutionWarnings substitutionWarningHandler = new DocumentSubstitutionWarnings();
            doc.WarningCallback = substitutionWarningHandler;

            List<FontSourceBase> fontSources = new List<FontSourceBase>(FontSettings.DefaultInstance.GetFontsSources());

            FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);
            fontSources.Add(folderFontSource);

            FontSourceBase[] updatedFontSources = fontSources.ToArray();
            FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

            doc.Save(ArtifactsDir + "WorkingWithFonts.GetSubstitutionWithoutSuffixes.pdf");

            Assert.AreEqual(
                "Font 'DINOT-Regular' has not been found. Using 'DINOT' font instead. Reason: font name substitution.",
                substitutionWarningHandler.FontWarnings[0].Description);
```


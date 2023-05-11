---
title: Receive Notifications Of Fonts
linktitle: Receive Notifications Of Fonts
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/receive-notifications-of-fonts/
---




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


---
title: Get Substitution Without Suffixes
linktitle: Get Substitution Without Suffixes
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/get-substitution-without-suffixes/
---




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


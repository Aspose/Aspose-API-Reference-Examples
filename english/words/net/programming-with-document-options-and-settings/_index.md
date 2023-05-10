---
title: Programming With Document Options And Settings
linktitle: Programming With Document Options And Settings
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain optimize for ms word, show grammatical and spelling errors, cleanup unused styles and lists, cleanup duplicate style, view options, document pa
type: docs
weight: 1510
url: /words/net/programming-with-document-options-and-settings/
---
Tutorials contain optimize for ms word, show grammatical and spelling errors, cleanup unused styles and lists, cleanup duplicate style, view options, document page setup, add japanese as editing languages, set russian as default editing language and set page setup and section formatting

## Optimize For Ms Word

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2016);

            doc.Save(ArtifactsDir + "WorkingWithDocumentOptionsAndSettings.OptimizeForMsWord.docx");
            
        
```

## Show Grammatical And Spelling Errors

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            doc.ShowGrammaticalErrors = true;
            doc.ShowSpellingErrors = true;

            doc.Save(ArtifactsDir + "WorkingWithDocumentOptionsAndSettings.ShowGrammaticalAndSpellingErrors.docx");
            
        
```

## Cleanup Unused Styles And Lists

```csharp

            
            Document doc = new Document(MyDir + "Unused styles.docx");

            // Combined with the built-in styles, the document now has eight styles.
            // A custom style is marked as "used" while there is any text within the document
            // formatted in that style. This means that the 4 styles we added are currently unused.
            Console.WriteLine($"Count of styles before Cleanup: {doc.Styles.Count}\n" +
                              $"Count of lists before Cleanup: {doc.Lists.Count}");

            // Cleans unused styles and lists from the document depending on given CleanupOptions. 
            CleanupOptions cleanupOptions = new CleanupOptions { UnusedLists = false, UnusedStyles = true };
            doc.Cleanup(cleanupOptions);

            Console.WriteLine($"Count of styles after Cleanup was decreased: {doc.Styles.Count}\n" +
                              $"Count of lists after Cleanup is the same: {doc.Lists.Count}");

            doc.Save(ArtifactsDir + "WorkingWithDocumentOptionsAndSettings.CleanupUnusedStylesAndLists.docx");
            
        
```

## Cleanup Duplicate Style

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            // Count of styles before Cleanup.
            Console.WriteLine(doc.Styles.Count);

            // Cleans duplicate styles from the document.
            CleanupOptions options = new CleanupOptions { DuplicateStyle = true };
            doc.Cleanup(options);

            // Count of styles after Cleanup was decreased.
            Console.WriteLine(doc.Styles.Count);

            doc.Save(ArtifactsDir + "WorkingWithDocumentOptionsAndSettings.CleanupDuplicateStyle.docx");
            
        
```

## View Options

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");
            
            doc.ViewOptions.ViewType = ViewType.PageLayout;
            doc.ViewOptions.ZoomPercent = 50;

            doc.Save(ArtifactsDir + "WorkingWithDocumentOptionsAndSettings.ViewOptions.docx");
            
        
```

## Document Page Setup

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            // Set the layout mode for a section allowing to define the document grid behavior.
            // Note that the Document Grid tab becomes visible in the Page Setup dialog of MS Word
            // if any Asian language is defined as editing language.
            doc.FirstSection.PageSetup.LayoutMode = SectionLayoutMode.Grid;
            doc.FirstSection.PageSetup.CharactersPerLine = 30;
            doc.FirstSection.PageSetup.LinesPerPage = 10;

            doc.Save(ArtifactsDir + "WorkingWithDocumentOptionsAndSettings.DocumentPageSetup.docx");
            
        
```

## Add Japanese As Editing Languages

```csharp

            
            LoadOptions loadOptions = new LoadOptions();
            
            // Set language preferences that will be used when document is loading.
            loadOptions.LanguagePreferences.AddEditingLanguage(EditingLanguage.Japanese);
            

            Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

            int localeIdFarEast = doc.Styles.DefaultFont.LocaleIdFarEast;
            Console.WriteLine(
                localeIdFarEast == (int) EditingLanguage.Japanese
                    ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
                    : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
        
```

## Set Russian As Default Editing Language

```csharp

            
            LoadOptions loadOptions = new LoadOptions();
            loadOptions.LanguagePreferences.DefaultEditingLanguage = EditingLanguage.Russian;

            Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

            int localeId = doc.Styles.DefaultFont.LocaleId;
            Console.WriteLine(
                localeId == (int) EditingLanguage.Russian
                    ? "The document either has no any language set in defaults or it was set to Russian originally."
                    : "The document default language was set to another than Russian language originally, so it is not overridden.");
            
        
```

## Set Page Setup And Section Formatting

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.PageSetup.Orientation = Orientation.Landscape;
            builder.PageSetup.LeftMargin = 50;
            builder.PageSetup.PaperSize = PaperSize.Paper10x14;

            doc.Save(ArtifactsDir + "WorkingWithDocumentOptionsAndSettings.SetPageSetupAndSectionFormatting.docx");
            
        
```


---
title: Document Page Setup
linktitle: Document Page Setup
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-options-and-settings/document-page-setup/
---




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


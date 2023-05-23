---
title: Set Page Setup And Section Formatting
linktitle: Set Page Setup And Section Formatting
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-options-and-settings/set-page-setup-and-section-formatting/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.PageSetup.Orientation = Orientation.Landscape;
            builder.PageSetup.LeftMargin = 50;
            builder.PageSetup.PaperSize = PaperSize.Paper10x14;

            doc.Save(ArtifactsDir + "WorkingWithDocumentOptionsAndSettings.SetPageSetupAndSectionFormatting.docx");
            
        
```


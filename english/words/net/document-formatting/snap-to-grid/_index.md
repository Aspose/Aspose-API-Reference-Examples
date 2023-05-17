---
title: Snap To Grid
linktitle: Snap To Grid
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-formatting/snap-to-grid/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Optimize the layout when typing in Asian characters.
            Paragraph par = doc.FirstSection.Body.FirstParagraph;
            par.ParagraphFormat.SnapToGrid = true;

            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod " +
                            "tempor incididunt ut labore et dolore magna aliqua.");
            
            par.Runs[0].Font.SnapToGrid = true;

            doc.Save(ArtifactsDir + "Paragraph.SnapToGrid.docx");
            
        
```


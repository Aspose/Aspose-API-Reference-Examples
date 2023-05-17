---
title: Change Asian Paragraph Spacing And Indents
linktitle: Change Asian Paragraph Spacing And Indents
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-formatting/change-asian-paragraph-spacing-and-indents/
---




```csharp

            
            Document doc = new Document(MyDir + "Asian typography.docx");

            ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
            format.CharacterUnitLeftIndent = 10;       // ParagraphFormat.LeftIndent will be updated
            format.CharacterUnitRightIndent = 10;      // ParagraphFormat.RightIndent will be updated
            format.CharacterUnitFirstLineIndent = 20;  // ParagraphFormat.FirstLineIndent will be updated
            format.LineUnitBefore = 5;                 // ParagraphFormat.SpaceBefore will be updated
            format.LineUnitAfter = 10;                 // ParagraphFormat.SpaceAfter will be updated

            doc.Save(ArtifactsDir + "DocumentFormatting.ChangeAsianParagraphSpacingAndIndents.doc");
            
        
```


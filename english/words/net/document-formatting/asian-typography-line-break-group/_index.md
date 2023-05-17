---
title: Asian Typography Line Break Group
linktitle: Asian Typography Line Break Group
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-formatting/asian-typography-line-break-group/
---




```csharp

            
            Document doc = new Document(MyDir + "Asian typography.docx");

            ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
            format.FarEastLineBreakControl = false;
            format.WordWrap = true;
            format.HangingPunctuation = false;

            doc.Save(ArtifactsDir + "DocumentFormatting.AsianTypographyLineBreakGroup.docx");
            
        
```


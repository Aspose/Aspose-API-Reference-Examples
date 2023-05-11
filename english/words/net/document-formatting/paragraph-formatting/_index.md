---
title: Paragraph Formatting
linktitle: Paragraph Formatting
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-formatting/paragraph-formatting/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            ParagraphFormat paragraphFormat = builder.ParagraphFormat;
            paragraphFormat.Alignment = ParagraphAlignment.Center;
            paragraphFormat.LeftIndent = 50;
            paragraphFormat.RightIndent = 50;
            paragraphFormat.SpaceAfter = 25;

            builder.Writeln(
                "I'm a very nice formatted paragraph. I'm intended to demonstrate how the left and right indents affect word wrapping.");
            builder.Writeln(
                "I'm another nice formatted paragraph. I'm intended to demonstrate how the space after paragraph looks like.");

            doc.Save(ArtifactsDir + "DocumentFormatting.ParagraphFormatting.docx");
            
        
```


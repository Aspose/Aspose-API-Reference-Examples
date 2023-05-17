---
title: Space Between Asian And Latin Text
linktitle: Space Between Asian And Latin Text
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-formatting/space-between-asian-and-latin-text/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            ParagraphFormat paragraphFormat = builder.ParagraphFormat;
            paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
            paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;

            builder.Writeln("Automatically adjust space between Asian and Latin text");
            builder.Writeln("Automatically adjust space between Asian text and numbers");

            doc.Save(ArtifactsDir + "DocumentFormatting.SpaceBetweenAsianAndLatinText.docx");
            
        
```


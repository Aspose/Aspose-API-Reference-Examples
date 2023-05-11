---
title: Insert Paragraph
linktitle: Insert Paragraph
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/insert-paragraph/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Font font = builder.Font;
            font.Size = 16;
            font.Bold = true;
            font.Color = Color.Blue;
            font.Name = "Arial";
            font.Underline = Underline.Dash;

            ParagraphFormat paragraphFormat = builder.ParagraphFormat;
            paragraphFormat.FirstLineIndent = 8;
            paragraphFormat.Alignment = ParagraphAlignment.Justify;
            paragraphFormat.KeepTogether = true;

            builder.Writeln("A whole paragraph.");

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.InsertParagraph.docx");
            
        
```


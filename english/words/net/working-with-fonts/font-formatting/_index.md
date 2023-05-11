---
title: Font Formatting
linktitle: Font Formatting
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/font-formatting/
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

            builder.Write("Sample text.");
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.FontFormatting.docx");
            
```


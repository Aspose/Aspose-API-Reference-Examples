---
title: Set Font Formatting
linktitle: Set Font Formatting
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/set-font-formatting/
---




```csharp
            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Font font = builder.Font;
            font.Bold = true;
            font.Color = Color.DarkBlue;
            font.Italic = true;
            font.Name = "Arial";
            font.Size = 24;
            font.Spacing = 5;
            font.Underline = Underline.Double;

            builder.Writeln("I'm a very nice formatted string.");
            
            doc.Save(ArtifactsDir + "WorkingWithFonts.SetFontFormatting.docx");
            
```

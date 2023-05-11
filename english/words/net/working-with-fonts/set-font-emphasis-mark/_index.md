---
title: Set Font Emphasis Mark
linktitle: Set Font Emphasis Mark
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/set-font-emphasis-mark/
---




```csharp
            
            Document document = new Document();
            DocumentBuilder builder = new DocumentBuilder(document);

            builder.Font.EmphasisMark = EmphasisMark.UnderSolidCircle;

            builder.Write("Emphasis text");
            builder.Writeln();
            builder.Font.ClearFormatting();
            builder.Write("Simple text");

            document.Save(ArtifactsDir + "WorkingWithFonts.SetFontEmphasisMark.docx");
            
```


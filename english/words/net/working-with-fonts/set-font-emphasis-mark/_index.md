---
title: Set Font Emphasis Mark
linktitle: Set Font Emphasis Mark
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/set-font-emphasis-mark/
---
### Sample source code for Set Font Emphasis Mark using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document document = new Document();
            DocumentBuilder builder = new DocumentBuilder(document);
            builder.Font.EmphasisMark = EmphasisMark.UnderSolidCircle;
            builder.Write("Emphasis text");
            builder.Writeln();
            builder.Font.ClearFormatting();
            builder.Write("Simple text");
            document.Save(dataDir + "WorkingWithFonts.SetFontEmphasisMark.docx");
```
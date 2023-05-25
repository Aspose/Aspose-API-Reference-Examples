---
title: Get Font Line Spacing
linktitle: Get Font Line Spacing
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/get-font-line-spacing/
---
### Sample source code for Get Font Line Spacing using Aspose.Words for .NET 
```csharp
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            builder.Font.Name = "Calibri";
            builder.Writeln("qText");
            Font font = builder.Document.FirstSection.Body.FirstParagraph.Runs[0].Font;
            Console.WriteLine($"lineSpacing = {font.LineSpacing}");
```
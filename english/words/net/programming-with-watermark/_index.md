---
title: Programming With Watermark
linktitle: Programming With Watermark
second_title: Aspose.Words for .NET API Reference
description: Examples contain add text watermark with specific options
type: docs
weight: 1570
url: /words/net/programming-with-watermark/
---
Examples contain add text watermark with specific options

## Add Text Watermark With Specific Options

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            TextWatermarkOptions options = new TextWatermarkOptions()
            {
                FontFamily = "Arial",
                FontSize = 36,
                Color = Color.Black,
                Layout = WatermarkLayout.Horizontal,
                IsSemitrasparent = false
            };

            doc.Watermark.SetText("Test", options);

            doc.Save(ArtifactsDir + "WorkWithWatermark.AddTextWatermarkWithSpecificOptions.docx");
            
        
```


---
title: Add Text Watermark With Specific Options
linktitle: Add Text Watermark With Specific Options
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-watermark/add-text-watermark-with-specific-options/
---




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


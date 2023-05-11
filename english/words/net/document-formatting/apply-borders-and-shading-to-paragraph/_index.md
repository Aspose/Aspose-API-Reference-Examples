---
title: Apply Borders And Shading To Paragraph
linktitle: Apply Borders And Shading To Paragraph
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-formatting/apply-borders-and-shading-to-paragraph/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            BorderCollection borders = builder.ParagraphFormat.Borders;
            borders.DistanceFromText = 20;
            borders[BorderType.Left].LineStyle = LineStyle.Double;
            borders[BorderType.Right].LineStyle = LineStyle.Double;
            borders[BorderType.Top].LineStyle = LineStyle.Double;
            borders[BorderType.Bottom].LineStyle = LineStyle.Double;

            Shading shading = builder.ParagraphFormat.Shading;
            shading.Texture = TextureIndex.TextureDiagonalCross;
            shading.BackgroundPatternColor = System.Drawing.Color.LightCoral;
            shading.ForegroundPatternColor = System.Drawing.Color.LightSalmon;

            builder.Write("I'm a formatted paragraph with double border and nice shading.");
            
            doc.Save(ArtifactsDir + "DocumentFormatting.ApplyBordersAndShadingToParagraph.doc");
            
        
```


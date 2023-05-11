---
title: Vertical Anchor
linktitle: Vertical Anchor
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-shapes/vertical-anchor/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Shape textBox = builder.InsertShape(ShapeType.TextBox, 200, 200);
            textBox.TextBox.VerticalAnchor = TextBoxAnchor.Bottom;
            
            builder.MoveTo(textBox.FirstParagraph);
            builder.Write("Textbox contents");

            doc.Save(ArtifactsDir + "WorkingWithShapes.VerticalAnchor.docx");
            
        
```


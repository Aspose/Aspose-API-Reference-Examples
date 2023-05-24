---
title: Vertical Anchor
linktitle: Vertical Anchor
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-shapes/vertical-anchor/
---
### Sample source code for Vertical Anchor using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape textBox = builder.InsertShape(ShapeType.TextBox, 200, 200);
            textBox.TextBox.VerticalAnchor = TextBoxAnchor.Bottom;
            builder.MoveTo(textBox.FirstParagraph);
            builder.Write("Textbox contents");
            doc.Save(dataDir + "WorkingWithShapes.VerticalAnchor.docx");
```
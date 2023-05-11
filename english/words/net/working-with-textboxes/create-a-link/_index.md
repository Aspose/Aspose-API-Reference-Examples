---
title: Create A Link
linktitle: Create A Link
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-textboxes/create-a-link/
---




```csharp
            Document doc = new Document();

            Shape shape1 = new Shape(doc, ShapeType.TextBox);
            Shape shape2 = new Shape(doc, ShapeType.TextBox);

            TextBox textBox1 = shape1.TextBox;
            TextBox textBox2 = shape2.TextBox;

            if (textBox1.IsValidLinkTarget(textBox2))
                textBox1.Next = textBox2;
            
```


---
title: Break A Link
linktitle: Break A Link
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-textboxes/break-a-link/
---




```csharp
            Document doc = new Document();

            Shape shape = new Shape(doc, ShapeType.TextBox);
            TextBox textBox = shape.TextBox;

            // Break a forward link.
            textBox.BreakForwardLink();

            // Break a forward link by setting a null.
            textBox.Next = null;

            // Break a link, which leads to this textbox.
            textBox.Previous?.BreakForwardLink();
            
```


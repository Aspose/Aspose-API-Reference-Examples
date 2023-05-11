---
title: Check Sequence
linktitle: Check Sequence
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-textboxes/check-sequence/
---




```csharp
            Document doc = new Document();

            Shape shape = new Shape(doc, ShapeType.TextBox);
            TextBox textBox = shape.TextBox;

            if (textBox.Next != null && textBox.Previous == null)
            {
                Console.WriteLine("The head of the sequence");
            }

            if (textBox.Next != null && textBox.Previous != null)
            {
                Console.WriteLine("The Middle of the sequence.");
            }

            if (textBox.Next == null && textBox.Previous != null)
            {
                Console.WriteLine("The Tail of the sequence.");
            }
            
```


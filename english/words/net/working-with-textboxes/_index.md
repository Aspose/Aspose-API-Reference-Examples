---
title: Working with Textboxes
linktitle: Working with Textboxes
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain create a link, check sequence, and break a link using Aspose.Words for .NET.
type: docs
weight: 1320
url: /words/net/working-with-textboxes/
---

The following tutorials contain create a link, check sequence, and break a link using Aspose.Words for .NET.

## Create A Link

```csharp
            Document doc = new Document();

            Shape shape1 = new Shape(doc, ShapeType.TextBox);
            Shape shape2 = new Shape(doc, ShapeType.TextBox);

            TextBox textBox1 = shape1.TextBox;
            TextBox textBox2 = shape2.TextBox;

            if (textBox1.IsValidLinkTarget(textBox2))
                textBox1.Next = textBox2;
            
```

## Check Sequence

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

## Break A Link

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


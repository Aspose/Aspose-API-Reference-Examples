---
title: working with textboxes
linktitle: working with textboxes
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 1320
url: /words/net/working-with-textboxes/
---

## Create ALink

```csharp
        {
            //ExStart:CreateALink
            Document doc = new Document();

            Shape shape1 = new Shape(doc, ShapeType.TextBox);
            Shape shape2 = new Shape(doc, ShapeType.TextBox);

            TextBox textBox1 = shape1.TextBox;
            TextBox textBox2 = shape2.TextBox;

            if (textBox1.IsValidLinkTarget(textBox2))
                textBox1.Next = textBox2;
            //ExEnd:CreateALink
        }

```

## Check Sequence

```csharp
        {
            //ExStart:CheckSequence
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
            //ExEnd:CheckSequence
        }

```

## Break ALink

```csharp
        {
            //ExStart:BreakALink
            Document doc = new Document();

            Shape shape = new Shape(doc, ShapeType.TextBox);
            TextBox textBox = shape.TextBox;

            // Break a forward link.
            textBox.BreakForwardLink();

            // Break a forward link by setting a null.
            textBox.Next = null;

            // Break a link, which leads to this textbox.
            textBox.Previous?.BreakForwardLink();
            //ExEnd:BreakALink
        }

```


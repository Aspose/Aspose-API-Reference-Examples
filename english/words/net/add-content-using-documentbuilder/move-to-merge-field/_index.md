---
title: Move To Merge Field
linktitle: Move To Merge Field
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/move-to-merge-field/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Insert a field using the DocumentBuilder and add a run of text after it.
            Field field = builder.InsertField("MERGEFIELD field");
            builder.Write(" Text after the field.");

            // The builder's cursor is currently at end of the document.
            Assert.Null(builder.CurrentNode);
            // We can move the builder to a field like this, placing the cursor at immediately after the field.
            builder.MoveToField(field, true);

            // Note that the cursor is at a place past the FieldEnd node of the field, meaning that we are not actually inside the field.
            // If we wish to move the DocumentBuilder to inside a field,
            // we will need to move it to a field's FieldStart or FieldSeparator node using the DocumentBuilder.MoveTo() method.
            Assert.AreEqual(field.End, builder.CurrentNode.PreviousSibling);
            builder.Write(" Text immediately after the field.");
            
        
```


---
title: Move To Section
linktitle: Move To Section
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/move-to-section/
---




```csharp

            
            Document doc = new Document();
            doc.AppendChild(new Section(doc));

            // Move a DocumentBuilder to the second section and add text.
            DocumentBuilder builder = new DocumentBuilder(doc);
            builder.MoveToSection(1);
            builder.Writeln("Text added to the 2nd section.");

            // Create document with paragraphs.
            doc = new Document(MyDir + "Paragraphs.docx");
            ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
            Assert.AreEqual(22, paragraphs.Count);

            // When we create a DocumentBuilder for a document, its cursor is at the very beginning of the document by default,
            // and any content added by the DocumentBuilder will just be prepended to the document.
            builder = new DocumentBuilder(doc);
            Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

            // You can move the cursor to any position in a paragraph.
            builder.MoveToParagraph(2, 10);
            Assert.AreEqual(2, paragraphs.IndexOf(builder.CurrentParagraph));
            builder.Writeln("This is a new third paragraph. ");
            Assert.AreEqual(3, paragraphs.IndexOf(builder.CurrentParagraph));
            
        
```


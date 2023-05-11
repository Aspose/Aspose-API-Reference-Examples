---
title: Owner Document
linktitle: Owner Document
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-node/owner-document/
---




```csharp
	Document doc = new Document();

	// Creating a new node of any type requires a document passed into the constructor.
	Paragraph para = new Paragraph(doc);

	// The new paragraph node does not yet have a parent.
	Console.WriteLine("Paragraph has no parent node: " + (para.ParentNode == null));

	// But the paragraph node knows its document.
	Console.WriteLine("Both nodes' documents are the same: " + (para.Document == doc));

	// The fact that a node always belongs to a document allows us to access and modify
	// properties that reference the document-wide data, such as styles or lists.
	para.ParagraphFormat.StyleName = "Heading 1";

	// Now add the paragraph to the main text of the first section.
	doc.FirstSection.Body.AppendChild(para);

	// The paragraph node is now a child of the Body node.
	Console.WriteLine("Paragraph has a parent node: " + (para.ParentNode != null));
            
```


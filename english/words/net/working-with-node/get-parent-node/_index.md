---
title: Get Parent Node
linktitle: Get Parent Node
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-node/get-parent-node/
---




```csharp
	Document doc = new Document();

	// The section is the first child node of the document.
	Node section = doc.FirstChild;

	// The section's parent node is the document.
	Console.WriteLine("Section parent is the document: " + (doc == section.ParentNode));
            
```


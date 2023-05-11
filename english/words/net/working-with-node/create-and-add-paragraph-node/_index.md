---
title: Create And Add Paragraph Node
linktitle: Create And Add Paragraph Node
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-node/create-and-add-paragraph-node/
---




```csharp
	Document doc = new Document();

	Paragraph para = new Paragraph(doc);

	Section section = doc.LastSection;
	section.Body.AppendChild(para);
            
```


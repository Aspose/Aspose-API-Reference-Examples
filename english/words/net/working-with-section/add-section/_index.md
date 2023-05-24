---
title: Add Section
linktitle: Add Section
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-section/add-section/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	builder.Writeln("Hello1");
	builder.Writeln("Hello2");

	Section sectionToAdd = new Section(doc);
	doc.Sections.Add(sectionToAdd);

```


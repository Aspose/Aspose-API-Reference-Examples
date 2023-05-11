---
title: Append Section Content
linktitle: Append Section Content
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-section/append-section-content/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	builder.Writeln("Hello1");
	doc.AppendChild(new Section(doc));
	builder.Writeln("Hello22");
	doc.AppendChild(new Section(doc));
	builder.Writeln("Hello3");
	doc.AppendChild(new Section(doc));
	builder.Writeln("Hello45");

	// This is the section that we will append and prepend to.
	Section section = doc.Sections[2];

	// This copies the content of the 1st section and inserts it at the beginning of the specified section.
	Section sectionToPrepend = doc.Sections[0];
	section.PrependContent(sectionToPrepend);

	// This copies the content of the 2nd section and inserts it at the end of the specified section.
	Section sectionToAppend = doc.Sections[1];
	section.AppendContent(sectionToAppend);
            
```


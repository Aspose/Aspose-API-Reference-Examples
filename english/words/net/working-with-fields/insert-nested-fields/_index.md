---
title: Insert Nested Fields
linktitle: Insert Nested Fields
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/insert-nested-fields/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	for (int i = 0; i < 5; i++)
		builder.InsertBreak(BreakType.PageBreak);

	builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);

	// We want to insert a field like this:
	// { IF {PAGE} <> {NUMPAGES} "See Next Page" "Last Page" }
	Field field = builder.InsertField(@"IF ");
	builder.MoveTo(field.Separator);
	builder.InsertField("PAGE");
	builder.Write(" <> ");
	builder.InsertField("NUMPAGES");
	builder.Write(" \"See Next Page\" \"Last Page\" ");

	field.Update();

	doc.Save(ArtifactsDir + "WorkingWithFields.InsertNestedFields.docx");
```


---
title: Insert Merge Field Using DOM
linktitle: Insert Merge Field Using DOM
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/insert-merge-field-using-dom/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	Paragraph para = (Paragraph) doc.GetChildNodes(NodeType.Paragraph, true)[0];

	builder.MoveTo(para);

	// We want to insert a merge field like this:
	// { " MERGEFIELD Test1 \\b Test2 \\f Test3 \\m \\v" }

	FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, false);

	// { " MERGEFIELD Test1" }
	field.FieldName = "Test1";

	// { " MERGEFIELD Test1 \\b Test2" }
	field.TextBefore = "Test2";

	// { " MERGEFIELD Test1 \\b Test2 \\f Test3 }
	field.TextAfter = "Test3";

	// { " MERGEFIELD Test1 \\b Test2 \\f Test3 \\m" }
	field.IsMapped = true;

	// { " MERGEFIELD Test1 \\b Test2 \\f Test3 \\m \\v" }
	field.IsVerticalFormatting = true;

	// Finally update this merge field
	field.Update();

	doc.Save(ArtifactsDir + "WorkingWithFields.InsertMergeFieldUsingDOM.docx");
```


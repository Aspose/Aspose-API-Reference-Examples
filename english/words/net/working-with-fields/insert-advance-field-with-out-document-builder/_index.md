---
title: Insert Advance Field With Out Document Builder
linktitle: Insert Advance Field With Out Document Builder
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/insert-advance-field-with-out-document-builder/
---




```csharp
	Document doc = new Document();

	Paragraph para = (Paragraph) doc.GetChildNodes(NodeType.Paragraph, true)[0];

	// We want to insert an Advance field like this:
	// { ADVANCE \\d 10 \\l 10 \\r -3.3 \\u 0 \\x 100 \\y 100 }

	FieldAdvance field = (FieldAdvance) para.AppendField(FieldType.FieldAdvance, false);
	
	// { ADVANCE \\d 10 " }
	field.DownOffset = "10";

	// { ADVANCE \\d 10 \\l 10 }
	field.LeftOffset = "10";

	// { ADVANCE \\d 10 \\l 10 \\r -3.3 }
	field.RightOffset = "-3.3";

	// { ADVANCE \\d 10 \\l 10 \\r -3.3 \\u 0 }
	field.UpOffset = "0";

	// { ADVANCE \\d 10 \\l 10 \\r -3.3 \\u 0 \\x 100 }
	field.HorizontalPosition = "100";

	// { ADVANCE \\d 10 \\l 10 \\r -3.3 \\u 0 \\x 100 \\y 100 }
	field.VerticalPosition = "100";

	field.Update();

	doc.Save(ArtifactsDir + "WorkingWithFields.InsertAdvanceFieldWithOutDocumentBuilder.docx");
```


---
title: Insert Field Using Field Builder
linktitle: Insert Field Using Field Builder
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/insert-field-using-field-builder/
---




```csharp
	Document doc = new Document();

	// Prepare IF field with two nested MERGEFIELD fields: { IF "left expression" = "right expression" "Firstname: { MERGEFIELD firstname }" "Lastname: { MERGEFIELD lastname }"}
	FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldIf)
		.AddArgument("left expression")
		.AddArgument("=")
		.AddArgument("right expression")
		.AddArgument(
			new FieldArgumentBuilder()
				.AddText("Firstname: ")
				.AddField(new FieldBuilder(FieldType.FieldMergeField).AddArgument("firstname")))
		.AddArgument(
			new FieldArgumentBuilder()
				.AddText("Lastname: ")
				.AddField(new FieldBuilder(FieldType.FieldMergeField).AddArgument("lastname")));

	// Insert IF field in exact location            
	Field field = fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);
	field.Update();

	doc.Save(ArtifactsDir + "Field.InsertFieldUsingFieldBuilder.docx");
```


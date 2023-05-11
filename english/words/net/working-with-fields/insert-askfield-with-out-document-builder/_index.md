---
title: Insert ASKField With Out Document Builder
linktitle: Insert ASKField With Out Document Builder
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/insert-askfield-with-out-document-builder/
---




```csharp
	Document doc = new Document();

	Paragraph para = (Paragraph) doc.GetChildNodes(NodeType.Paragraph, true)[0];

	// We want to insert an Ask field like this:
	// { ASK \"Test 1\" Test2 \\d Test3 \\o }

	FieldAsk field = (FieldAsk) para.AppendField(FieldType.FieldAsk, false);

	// { ASK \"Test 1\" " }
	field.BookmarkName = "Test 1";

	// { ASK \"Test 1\" Test2 }
	field.PromptText = "Test2";

	// { ASK \"Test 1\" Test2 \\d Test3 }
	field.DefaultResponse = "Test3";

	// { ASK \"Test 1\" Test2 \\d Test3 \\o }
	field.PromptOnceOnMailMerge = true;

	field.Update();

	doc.Save(ArtifactsDir + "WorkingWithFields.InsertASKFieldWithOutDocumentBuilder.docx");
```


---
title: Insert Mail Merge Address Block Field Using DOM
linktitle: Insert Mail Merge Address Block Field Using DOM
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/insert-mail-merge-address-block-field-using-dom/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	Paragraph para = (Paragraph) doc.GetChildNodes(NodeType.Paragraph, true)[0];

	builder.MoveTo(para);

	// We want to insert a mail merge address block like this:
	// { ADDRESSBLOCK \\c 1 \\d \\e Test2 \\f Test3 \\l \"Test 4\" }

	FieldAddressBlock field = (FieldAddressBlock) builder.InsertField(FieldType.FieldAddressBlock, false);

	// { ADDRESSBLOCK \\c 1" }
	field.IncludeCountryOrRegionName = "1";

	// { ADDRESSBLOCK \\c 1 \\d" }
	field.FormatAddressOnCountryOrRegion = true;

	// { ADDRESSBLOCK \\c 1 \\d \\e Test2 }
	field.ExcludedCountryOrRegionName = "Test2";

	// { ADDRESSBLOCK \\c 1 \\d \\e Test2 \\f Test3 }
	field.NameAndAddressFormat = "Test3";

	// { ADDRESSBLOCK \\c 1 \\d \\e Test2 \\f Test3 \\l \"Test 4\" }
	field.LanguageId = "Test 4";

	field.Update();

	doc.Save(ArtifactsDir + "WorkingWithFields.InsertMailMergeAddressBlockFieldUsingDOM.docx");
```


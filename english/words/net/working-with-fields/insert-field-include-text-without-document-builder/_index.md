---
title: Insert Field Include Text Without Document Builder
linktitle: Insert Field Include Text Without Document Builder
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/insert-field-include-text-without-document-builder/
---




```csharp
	Document doc = new Document();

	Paragraph para = new Paragraph(doc);

	// We want to insert an INCLUDETEXT field like this:
	// { INCLUDETEXT  "file path" }

	FieldIncludeText fieldIncludeText = (FieldIncludeText) para.AppendField(FieldType.FieldIncludeText, false);
	fieldIncludeText.BookmarkName = "bookmark";
	fieldIncludeText.SourceFullName = MyDir + "IncludeText.docx";

	doc.FirstSection.Body.AppendChild(para);

	fieldIncludeText.Update();

	doc.Save(ArtifactsDir + "WorkingWithFields.InsertIncludeFieldWithoutDocumentBuilder.docx");
```


---
title: Insert TOAField Without Document Builder
linktitle: Insert TOAField Without Document Builder
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/insert-toafield-without-document-builder/
---




```csharp
	Document doc = new Document();
	Paragraph para = new Paragraph(doc);

	// We want to insert TA and TOA fields like this:
	// { TA  \c 1 \l "Value 0" }
	// { TOA  \c 1 }

	FieldTA fieldTA = (FieldTA) para.AppendField(FieldType.FieldTOAEntry, false);
	fieldTA.EntryCategory = "1";
	fieldTA.LongCitation = "Value 0";

	doc.FirstSection.Body.AppendChild(para);

	para = new Paragraph(doc);

	FieldToa fieldToa = (FieldToa) para.AppendField(FieldType.FieldTOA, false);
	fieldToa.EntryCategory = "1";
	doc.FirstSection.Body.AppendChild(para);

	fieldToa.Update();

	doc.Save(ArtifactsDir + "WorkingWithFields.InsertTOAFieldWithoutDocumentBuilder.docx");
```


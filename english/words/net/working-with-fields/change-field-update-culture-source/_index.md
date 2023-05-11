---
title: Change Field Update Culture Source
linktitle: Change Field Update Culture Source
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/change-field-update-culture-source/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	// Insert content with German locale.
	builder.Font.LocaleId = 1031;
	builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
	builder.Write(" - ");
	builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");
	

	// Shows how to specify where the culture used for date formatting during field update and mail merge is chosen from
	// set the culture used during field update to the culture used by the field.
	doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
	doc.MailMerge.Execute(new string[] { "Date2" }, new object[] { new DateTime(2011, 1, 01) });
	
	doc.Save(ArtifactsDir + "WorkingWithFields.ChangeFieldUpdateCultureSource.docx");
```


---
title: Field Update Culture
linktitle: Field Update Culture
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/field-update-culture/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	builder.InsertField(FieldType.FieldTime, true);

	doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
	doc.FieldOptions.FieldUpdateCultureProvider = new FieldUpdateCultureProvider();

	doc.Save(ArtifactsDir + "WorkingWithFields.FieldUpdateCulture.pdf");
```


---
title: Insert Field None
linktitle: Insert Field None
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/insert-field-none/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	FieldUnknown field = (FieldUnknown) builder.InsertField(FieldType.FieldNone, false);

	doc.Save(ArtifactsDir + "WorkingWithFields.InsertFieldNone.docx");
```


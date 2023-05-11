---
title: Convert Fields In Body
linktitle: Convert Fields In Body
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/convert-fields-in-body/
---




```csharp
	Document doc = new Document(MyDir + "Linked fields.docx");

	// Pass the appropriate parameters to convert PAGE fields encountered to text only in the body of the first section.
	doc.FirstSection.Body.Range.Fields.Where(f => f.Type == FieldType.FieldPage).ToList().ForEach(f => f.Unlink());

	doc.Save(ArtifactsDir + "WorkingWithFields.ConvertFieldsInBody.docx");
```


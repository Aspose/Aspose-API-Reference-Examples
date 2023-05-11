---
title: Form Fields Work With Properties
linktitle: Form Fields Work With Properties
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-formfields/form-fields-work-with-properties/
---




```csharp
	Document doc = new Document(MyDir + "Form fields.docx");
	FormField formField = doc.Range.FormFields[3];

	if (formField.Type == FieldType.FieldFormTextInput)
		formField.Result = "My name is " + formField.Name;
	
```


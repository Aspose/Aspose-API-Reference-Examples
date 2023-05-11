---
title: Form Fields Get By Name
linktitle: Form Fields Get By Name
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-formfields/form-fields-get-by-name/
---




```csharp
            
	Document doc = new Document(MyDir + "Form fields.docx");

	FormFieldCollection documentFormFields = doc.Range.FormFields;

	FormField formField1 = documentFormFields[3];
	FormField formField2 = documentFormFields["Text2"];
	

	formField1.Font.Size = 20;
	formField2.Font.Color = Color.Red;
            
```


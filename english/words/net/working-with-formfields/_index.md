---
title: Working with FormFields
linktitle: Working with FormFields
second_title: Aspose.Words for .NET API Reference
description: Examples containing how insert form fileds, working with form fileds' properties, get form fields collection, and get form fields get by name in Word Document using Aspose.Words for .NET.
type: docs
weight: 690
url: /words/net/working-with-formfields/
---
The following examples show how insert form fileds, working with form fileds' properties, get form fields collection, and get form fields get by name in Word Document using Aspose.Words for .NET.

## Insert Form Fields

```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	string[] items = { "One", "Two", "Three" };
	builder.InsertComboBox("DropDown", items, 0);
            
```

## Form Fields Work With Properties

```csharp
	Document doc = new Document(MyDir + "Form fields.docx");
	FormField formField = doc.Range.FormFields[3];

	if (formField.Type == FieldType.FieldFormTextInput)
		formField.Result = "My name is " + formField.Name;
	
```

## Form Fields Get Form Fields Collection

```csharp
	Document doc = new Document(MyDir + "Form fields.docx");
	
	FormFieldCollection formFields = doc.Range.FormFields;
	
```

## Form Fields Get By Name

```csharp
            
	Document doc = new Document(MyDir + "Form fields.docx");

	FormFieldCollection documentFormFields = doc.Range.FormFields;

	FormField formField1 = documentFormFields[3];
	FormField formField2 = documentFormFields["Text2"];
	

	formField1.Font.Size = 20;
	formField2.Font.Color = Color.Red;
            
```


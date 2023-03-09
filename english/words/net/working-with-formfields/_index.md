---
title: working with formfields
linktitle: working with formfields
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 690
url: /words/net/working-with-formfields/
---

## Insert Form Fields

```csharp
        {
            //ExStart:InsertFormFields
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            string[] items = { "One", "Two", "Three" };
            builder.InsertComboBox("DropDown", items, 0);
            //ExEnd:InsertFormFields
        }

```

## Form Fields Work With Properties

```csharp
        {
            //ExStart:FormFieldsWorkWithProperties
            Document doc = new Document(MyDir + "Form fields.docx");
            FormField formField = doc.Range.FormFields[3];

            if (formField.Type == FieldType.FieldFormTextInput)
                formField.Result = "My name is " + formField.Name;
            //ExEnd:FormFieldsWorkWithProperties            
        }

```

## Form Fields Get Form Fields Collection

```csharp
        {
            //ExStart:FormFieldsGetFormFieldsCollection
            Document doc = new Document(MyDir + "Form fields.docx");
            
            FormFieldCollection formFields = doc.Range.FormFields;
            //ExEnd:FormFieldsGetFormFieldsCollection
        }

```

## Form Fields Get By Name

```csharp
        {
            //ExStart:FormFieldsFontFormatting
            //ExStart:FormFieldsGetByName
            Document doc = new Document(MyDir + "Form fields.docx");

            FormFieldCollection documentFormFields = doc.Range.FormFields;

            FormField formField1 = documentFormFields[3];
            FormField formField2 = documentFormFields["Text2"];
            //ExEnd:FormFieldsGetByName

            formField1.Font.Size = 20;
            formField2.Font.Color = Color.Red;
            //ExEnd:FormFieldsFontFormatting
        }

```


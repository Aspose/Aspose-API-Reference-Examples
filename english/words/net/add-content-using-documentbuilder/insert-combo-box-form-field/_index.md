---
title: Insert Combo Box Form Field
linktitle: Insert Combo Box Form Field
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/insert-combo-box-form-field/
---




```csharp

            
            string[] items = { "One", "Two", "Three" };

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertComboBox("DropDown", items, 0);

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.InsertComboBoxFormField.docx");
            
        
```


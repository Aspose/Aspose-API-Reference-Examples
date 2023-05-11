---
title: Insert Text Input Form Field
linktitle: Insert Text Input Form Field
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/insert-text-input-form-field/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.InsertTextInput("TextInput", TextFormFieldType.Regular, "", "Hello", 0);

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.InsertTextInputFormField.docx");
            
        
```


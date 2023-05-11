---
title: Insert Check Box Form Field
linktitle: Insert Check Box Form Field
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/insert-check-box-form-field/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.InsertCheckBox("CheckBox", true, true, 0);

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.InsertCheckBoxFormField.docx");
            
        
```


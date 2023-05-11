---
title: Insert TCField
linktitle: Insert TCField
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/insert-tcfield/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertField("TC \"Entry Text\" \\f t");

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.InsertTCField.docx");
            
        
```


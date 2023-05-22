---
title: Encrypt Document With Password
linktitle: Encrypt Document With Password
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-docsaveoptions/encrypt-document-with-password/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.Write("Hello world!");

            DocSaveOptions saveOptions = new DocSaveOptions { Password = "password" };

            doc.Save(ArtifactsDir + "WorkingWithDocSaveOptions.EncryptDocumentWithPassword.docx", saveOptions);
            
        
```


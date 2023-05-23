---
title: Encrypt Docx With Password
linktitle: Encrypt Docx With Password
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-ooxmlsaveoptions/encrypt-docx-with-password/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "password" };

            doc.Save(ArtifactsDir + "WorkingWithOoxmlSaveOptions.EncryptDocxWithPassword.docx", saveOptions);
            
        
```


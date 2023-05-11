---
title: Load Encrypted Document
linktitle: Load Encrypted Document
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-loadoptions/load-encrypted-document/
---




```csharp

            
            
            Document doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));
            

            doc.Save(ArtifactsDir + "WorkingWithLoadOptions.LoadAndSaveEncryptedOdt.odt", new OdtSaveOptions("newPassword"));
            
        
```


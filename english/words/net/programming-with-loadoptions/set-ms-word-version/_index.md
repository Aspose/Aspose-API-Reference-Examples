---
title: Set Ms Word Version
linktitle: Set Ms Word Version
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-loadoptions/set-ms-word-version/
---




```csharp

            
            // Create a new LoadOptions object, which will load documents according to MS Word 2019 specification by default
            // and change the loading version to Microsoft Word 2010.
            LoadOptions loadOptions = new LoadOptions { MswVersion = MsWordVersion.Word2010 };
            
            Document doc = new Document(MyDir + "Document.docx", loadOptions);

            doc.Save(ArtifactsDir + "WorkingWithLoadOptions.SetMsWordVersion.docx");
            
        
```


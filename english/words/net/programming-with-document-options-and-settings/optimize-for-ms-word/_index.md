---
title: Optimize For Ms Word
linktitle: Optimize For Ms Word
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-options-and-settings/optimize-for-ms-word/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2016);

            doc.Save(ArtifactsDir + "WorkingWithDocumentOptionsAndSettings.OptimizeForMsWord.docx");
            
        
```


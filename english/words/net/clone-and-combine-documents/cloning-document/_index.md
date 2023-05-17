---
title: Cloning Document
linktitle: Cloning Document
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/clone-and-combine-documents/cloning-document/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            Document clone = doc.Clone();
            clone.Save(ArtifactsDir + "CloneAndCombineDocuments.CloningDocument.docx");
            
        
```


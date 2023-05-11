---
title: Clear Contents Control
linktitle: Clear Contents Control
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/clear-contents-control/
---




```csharp

            
            Document doc = new Document(MyDir + "Structured document tags.docx");

            StructuredDocumentTag sdt = (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);
            sdt.Clear();

            doc.Save(ArtifactsDir + "WorkingWithSdt.ClearContentsControl.doc");
            
        
```


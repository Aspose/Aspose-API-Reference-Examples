---
title: Set Content Control Color
linktitle: Set Content Control Color
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/set-content-control-color/
---




```csharp

            
            Document doc = new Document(MyDir + "Structured document tags.docx");

            StructuredDocumentTag sdt = (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);
            sdt.Color = Color.Red;

            doc.Save(ArtifactsDir + "WorkingWithSdt.SetContentControlColor.docx");
            
        
```

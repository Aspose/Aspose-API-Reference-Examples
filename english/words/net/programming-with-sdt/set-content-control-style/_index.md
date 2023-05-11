---
title: Set Content Control Style
linktitle: Set Content Control Style
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/set-content-control-style/
---




```csharp

            
            Document doc = new Document(MyDir + "Structured document tags.docx");

            StructuredDocumentTag sdt = (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);
            Style style = doc.Styles[StyleIdentifier.Quote];
            sdt.Style = style;

            doc.Save(ArtifactsDir + "WorkingWithSdt.SetContentControlStyle.docx");
            
        
```


---
title: Multi Section
linktitle: Multi Section
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/multi-section/
---




```csharp

            
            Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

            NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true);

            foreach (StructuredDocumentTagRangeStart tag in tags)
                Console.WriteLine(tag.Title);
            
        
```


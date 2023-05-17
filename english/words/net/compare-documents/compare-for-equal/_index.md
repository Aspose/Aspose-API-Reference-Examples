---
title: Compare For Equal
linktitle: Compare For Equal
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/compare-documents/compare-for-equal/
---




```csharp

            
            Document docA = new Document(MyDir + "Document.docx");
            Document docB = docA.Clone();
            
            // DocA now contains changes as revisions.
            docA.Compare(docB, "user", DateTime.Now);

            Console.WriteLine(docA.Revisions.Count == 0 ? "Documents are equal" : "Documents are not equal");
            
        
```


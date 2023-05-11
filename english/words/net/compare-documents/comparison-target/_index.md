---
title: Comparison Target
linktitle: Comparison Target
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/compare-documents/comparison-target/
---




```csharp

            
            Document docA = new Document(MyDir + "Document.docx");
            Document docB = docA.Clone();

            // Relates to Microsoft Word "Show changes in" option in "Compare Documents" dialog box.
            CompareOptions options = new CompareOptions { IgnoreFormatting = true, Target = ComparisonTargetType.New };

            docA.Compare(docB, "user", DateTime.Now, options);
            
        
```


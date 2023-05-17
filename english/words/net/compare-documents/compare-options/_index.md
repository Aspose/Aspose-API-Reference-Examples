---
title: Compare Options
linktitle: Compare Options
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/compare-documents/compare-options/
---




```csharp

            
            Document docA = new Document(MyDir + "Document.docx");
            Document docB = docA.Clone();

            CompareOptions options = new CompareOptions
            {
                IgnoreFormatting = true,
                IgnoreHeadersAndFooters = true,
                IgnoreCaseChanges = true,
                IgnoreTables = true,
                IgnoreFields = true,
                IgnoreComments = true,
                IgnoreTextboxes = true,
                IgnoreFootnotes = true
            };

            docA.Compare(docB, "user", DateTime.Now, options);

            Console.WriteLine(docA.Revisions.Count == 0 ? "Documents are equal" : "Documents are not equal");
            
        
```


---
title: Comparison Granularity
linktitle: Comparison Granularity
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/compare-documents/comparison-granularity/
---




```csharp

            
            DocumentBuilder builderA = new DocumentBuilder(new Document());
            DocumentBuilder builderB = new DocumentBuilder(new Document());

            builderA.Writeln("This is A simple word");
            builderB.Writeln("This is B simple words");

            CompareOptions compareOptions = new CompareOptions { Granularity = Granularity.CharLevel };

            builderA.Document.Compare(builderB.Document, "author", DateTime.Now, compareOptions);
            
        
```


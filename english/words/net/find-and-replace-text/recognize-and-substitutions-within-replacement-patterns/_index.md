---
title: Recognize And Substitutions Within Replacement Patterns
linktitle: Recognize And Substitutions Within Replacement Patterns
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/find-and-replace-text/recognize-and-substitutions-within-replacement-patterns/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Write("Jason give money to Paul.");

            Regex regex = new Regex(@"([A-z]+) give money to ([A-z]+)");

            FindReplaceOptions options = new FindReplaceOptions { UseSubstitutions = true };

            doc.Range.Replace(regex, @"$2 take money from $1", options);
            
        
```


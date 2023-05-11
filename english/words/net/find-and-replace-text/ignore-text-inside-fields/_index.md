---
title: Ignore Text Inside Fields
linktitle: Ignore Text Inside Fields
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/find-and-replace-text/ignore-text-inside-fields/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Insert field with text inside.
            builder.InsertField("INCLUDETEXT", "Text in field");
            
            FindReplaceOptions options = new FindReplaceOptions { IgnoreFields = true };
            
            Regex regex = new Regex("e");
            doc.Range.Replace(regex, "*", options);
            
            Console.WriteLine(doc.GetText());

            options.IgnoreFields = false;
            doc.Range.Replace(regex, "*", options);
            
            Console.WriteLine(doc.GetText());
            
        
```


---
title: Ignore Text Inside Insert Revisions
linktitle: Ignore Text Inside Insert Revisions
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/find-and-replace-text/ignore-text-inside-insert-revisions/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Insert text with tracking revisions.
            doc.StartTrackRevisions("author", DateTime.Now);
            builder.Writeln("Inserted");
            doc.StopTrackRevisions();

            // Insert non-revised text.
            builder.Write("Text");

            FindReplaceOptions options = new FindReplaceOptions { IgnoreInserted = true };

            Regex regex = new Regex("e");
            doc.Range.Replace(regex, "*", options);
            
            Console.WriteLine(doc.GetText());

            options.IgnoreInserted = false;
            doc.Range.Replace(regex, "*", options);
            
            Console.WriteLine(doc.GetText());
            
        
```


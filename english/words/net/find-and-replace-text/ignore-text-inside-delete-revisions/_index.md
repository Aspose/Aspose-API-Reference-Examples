---
title: Ignore Text Inside Delete Revisions
linktitle: Ignore Text Inside Delete Revisions
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/find-and-replace-text/ignore-text-inside-delete-revisions/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Insert non-revised text.
            builder.Writeln("Deleted");
            builder.Write("Text");

            // Remove first paragraph with tracking revisions.
            doc.StartTrackRevisions("author", DateTime.Now);
            doc.FirstSection.Body.FirstParagraph.Remove();
            doc.StopTrackRevisions();

            FindReplaceOptions options = new FindReplaceOptions { IgnoreDeleted = true };

            Regex regex = new Regex("e");
            doc.Range.Replace(regex, "*", options);

            Console.WriteLine(doc.GetText());

            options.IgnoreDeleted = false;
            doc.Range.Replace(regex, "*", options);

            Console.WriteLine(doc.GetText());
            
        
```


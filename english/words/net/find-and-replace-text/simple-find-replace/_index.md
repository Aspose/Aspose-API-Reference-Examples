---
title: Simple Find Replace
linktitle: Simple Find Replace
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/find-and-replace-text/simple-find-replace/
---




```csharp

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Hello _CustomerName_,");
            Console.WriteLine("Original document text: " + doc.Range.Text);

            doc.Range.Replace("_CustomerName_", "James Bond", new FindReplaceOptions(FindReplaceDirection.Forward));

            Console.WriteLine("Document text after replace: " + doc.Range.Text);

            // Save the modified document
            doc.Save(ArtifactsDir + "FindAndReplace.SimpleFindReplace.docx");
        
```


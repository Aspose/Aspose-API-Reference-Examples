---
title: Replace With Regex
linktitle: Replace With Regex
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/find-and-replace-text/replace-with-regex/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.Writeln("sad mad bad");

            FindReplaceOptions options = new FindReplaceOptions();

            doc.Range.Replace(new Regex("[s|m]ad"), "bad", options);

            doc.Save(ArtifactsDir + "FindAndReplace.ReplaceWithRegex.docx");
            
        
```


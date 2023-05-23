---
title: Replace With String
linktitle: Replace With String
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/find-and-replace-text/replace-with-string/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.Writeln("sad mad bad");

            doc.Range.Replace("sad", "bad", new FindReplaceOptions(FindReplaceDirection.Forward));

            doc.Save(ArtifactsDir + "FindAndReplace.ReplaceWithString.docx");
            
        
```


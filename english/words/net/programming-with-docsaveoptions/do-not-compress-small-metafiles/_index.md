---
title: Do Not Compress Small Metafiles
linktitle: Do Not Compress Small Metafiles
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-docsaveoptions/do-not-compress-small-metafiles/
---




```csharp

            
            Document doc = new Document(MyDir + "Microsoft equation object.docx");

            DocSaveOptions saveOptions = new DocSaveOptions { AlwaysCompressMetafiles = false };

            doc.Save(ArtifactsDir + "WorkingWithDocSaveOptions.NotCompressSmallMetafiles.docx", saveOptions);
            
        
```


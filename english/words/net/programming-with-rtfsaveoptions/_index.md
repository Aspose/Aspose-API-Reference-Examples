---
title: Programming With Rtfsaveoptions
linktitle: Programming With Rtfsaveoptions
second_title: Aspose.Words for .NET API Reference
description: Examples contain saving images as wmf
type: docs
weight: 1690
url: /words/net/programming-with-rtfsaveoptions/
---
Examples contain saving images as wmf

## Saving Images As Wmf

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            RtfSaveOptions saveOptions = new RtfSaveOptions { SaveImagesAsWmf = true };

            doc.Save(ArtifactsDir + "WorkingWithRtfSaveOptions.SavingImagesAsWmf.rtf", saveOptions);
            
        
```


---
title: Saving Images As Wmf
linktitle: Saving Images As Wmf
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-rtfsaveoptions/saving-images-as-wmf/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            RtfSaveOptions saveOptions = new RtfSaveOptions { SaveImagesAsWmf = true };

            doc.Save(ArtifactsDir + "WorkingWithRtfSaveOptions.SavingImagesAsWmf.rtf", saveOptions);
            
        
```


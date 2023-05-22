---
title: Do Not Save Picture Bullet
linktitle: Do Not Save Picture Bullet
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-docsaveoptions/do-not-save-picture-bullet/
---




```csharp

            
            Document doc = new Document(MyDir + "Image bullet points.docx");

            DocSaveOptions saveOptions = new DocSaveOptions { SavePictureBullet = false };

            doc.Save(ArtifactsDir + "WorkingWithDocSaveOptions.DoNotSavePictureBullet.docx", saveOptions);
            
        
```


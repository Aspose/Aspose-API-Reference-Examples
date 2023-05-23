---
title: Page Saving Callback
linktitle: Page Saving Callback
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-imagesaveoptions/page-saving-callback/
---




```csharp

            Document doc = new Document(MyDir + "Rendering.docx");

            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png)
            {
                PageSet = new PageSet(new PageRange(0, doc.PageCount - 1)),
                PageSavingCallback = new HandlePageSavingCallback()
            };

            doc.Save(ArtifactsDir + "WorkingWithImageSaveOptions.PageSavingCallback.png", imageSaveOptions);
        
```


---
title: Set Images Folder
linktitle: Set Images Folder
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-markdownsaveoptions/set-images-folder/
---




```csharp

            
            Document doc = new Document(MyDir + "Image bullet points.docx");

            MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { ImagesFolder = ArtifactsDir + "Images" };

            using (MemoryStream stream = new MemoryStream())
                doc.Save(stream, saveOptions);
            
        
```


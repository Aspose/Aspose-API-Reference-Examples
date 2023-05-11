---
title: Insert Floating Image
linktitle: Insert Floating Image
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/insert-floating-image/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertImage(ImagesDir + "Transparent background logo.png",
                RelativeHorizontalPosition.Margin,
                100,
                RelativeVerticalPosition.Margin,
                100,
                200,
                100,
                WrapType.Square);

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.InsertFloatingImage.docx");
            
        
```


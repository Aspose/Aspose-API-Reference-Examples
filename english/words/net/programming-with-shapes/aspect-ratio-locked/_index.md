---
title: Aspect Ratio Locked
linktitle: Aspect Ratio Locked
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-shapes/aspect-ratio-locked/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Shape shape = builder.InsertImage(ImagesDir + "Transparent background logo.png");
            shape.AspectRatioLocked = false;

            doc.Save(ArtifactsDir + "WorkingWithShapes.AspectRatioLocked.docx");
            
        
```


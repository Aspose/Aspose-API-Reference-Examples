---
title: Get Actual Shape Bounds Points
linktitle: Get Actual Shape Bounds Points
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-shapes/get-actual-shape-bounds-points/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Shape shape = builder.InsertImage(ImagesDir + "Transparent background logo.png");
            shape.AspectRatioLocked = false;

            Console.Write("\nGets the actual bounds of the shape in points: ");
            Console.WriteLine(shape.GetShapeRenderer().BoundsInPoints);
            
        
```


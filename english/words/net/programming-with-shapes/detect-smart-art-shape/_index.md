---
title: Detect Smart Art Shape
linktitle: Detect Smart Art Shape
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-shapes/detect-smart-art-shape/
---




```csharp

            
            Document doc = new Document(MyDir + "SmartArt.docx");

            int count = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

            Console.WriteLine("The document has {0} shapes with SmartArt.", count);
            
        
```


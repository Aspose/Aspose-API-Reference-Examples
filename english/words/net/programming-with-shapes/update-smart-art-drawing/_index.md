---
title: Update Smart Art Drawing
linktitle: Update Smart Art Drawing
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-shapes/update-smart-art-drawing/
---




```csharp

            Document doc = new Document(MyDir + "SmartArt.docx");

            
            foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true))
                if (shape.HasSmartArt)
                    shape.UpdateSmartArtDrawing();
            
        
```


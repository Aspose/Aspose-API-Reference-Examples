---
title: Update Smart Art Drawing
linktitle: Update Smart Art Drawing
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-shapes/update-smart-art-drawing/
---
### Sample source code for Update Smart Art Drawing using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "SmartArt.docx");
            foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true))
                if (shape.HasSmartArt)
                    shape.UpdateSmartArtDrawing();
```
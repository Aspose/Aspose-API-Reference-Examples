---
title: Image
linktitle: Image
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-markdown/image/
---




```csharp
	// Use a document builder to add content to the document.
	DocumentBuilder builder = new DocumentBuilder();

	// Insert image.
	Shape shape = new Shape(builder.Document, ShapeType.Image);
	shape.WrapType = WrapType.Inline;
	shape.ImageData.SourceFullName = "/attachment/1456/pic001.png";
	shape.ImageData.Title = "title";
	builder.InsertNode(shape);
            
```


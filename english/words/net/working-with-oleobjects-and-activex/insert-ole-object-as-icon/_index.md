---
title: Insert Ole Object As Icon
linktitle: Insert Ole Object As Icon
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-oleobjects-and-activex/insert-ole-object-as-icon/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImagesDir + "Logo icon.ico",
		"My embedded file");

	doc.Save(ArtifactsDir + "WorkingWithOleObjectsAndActiveX.InsertOleObjectAsIcon.docx");
            
```


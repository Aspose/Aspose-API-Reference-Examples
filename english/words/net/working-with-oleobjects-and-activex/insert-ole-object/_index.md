---
title: Insert Ole Object
linktitle: Insert Ole Object
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-oleobjects-and-activex/insert-ole-object/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	builder.InsertOleObject("http://www.aspose.com", "htmlfile", true, true, null);

	doc.Save(ArtifactsDir + "WorkingWithOleObjectsAndActiveX.InsertOleObject.docx");
            
```


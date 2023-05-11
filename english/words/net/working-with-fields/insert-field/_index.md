---
title: Insert Field
linktitle: Insert Field
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/insert-field/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);
	
	builder.InsertField(@"MERGEFIELD MyFieldName \* MERGEFORMAT");
	
	doc.Save(ArtifactsDir + "WorkingWithFields.InsertField.docx");
```


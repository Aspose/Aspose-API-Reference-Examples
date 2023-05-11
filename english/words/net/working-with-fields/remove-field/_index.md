---
title: Remove Field
linktitle: Remove Field
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/remove-field/
---




```csharp
	Document doc = new Document(MyDir + "Various fields.docx");
	
	Field field = doc.Range.Fields[0];
	field.Remove();
```


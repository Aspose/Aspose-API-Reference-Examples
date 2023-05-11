---
title: Field Code
linktitle: Field Code
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/field-code/
---




```csharp
	Document doc = new Document(MyDir + "Hyperlinks.docx");

	foreach (Field field in doc.Range.Fields)
	{
		string fieldCode = field.GetFieldCode();
		string fieldResult = field.Result;
	}
```


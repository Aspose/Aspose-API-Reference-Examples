---
title: Field Display Results
linktitle: Field Display Results
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/field-display-results/
---




```csharp
	Document document = new Document(MyDir + "Various fields.docx");

	document.UpdateFields();
	

	foreach (Field field in document.Range.Fields)
		Console.WriteLine(field.DisplayResult);
```


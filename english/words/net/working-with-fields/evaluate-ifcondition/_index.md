---
title: Evaluate IFCondition
linktitle: Evaluate IFCondition
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/evaluate-ifcondition/
---




```csharp
	DocumentBuilder builder = new DocumentBuilder();

	FieldIf field = (FieldIf) builder.InsertField("IF 1 = 1", null);
	FieldIfComparisonResult actualResult = field.EvaluateCondition();

	Console.WriteLine(actualResult);
```


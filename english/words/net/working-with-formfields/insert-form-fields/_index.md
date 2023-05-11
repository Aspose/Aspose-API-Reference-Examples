---
title: Insert Form Fields
linktitle: Insert Form Fields
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-formfields/insert-form-fields/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	string[] items = { "One", "Two", "Three" };
	builder.InsertComboBox("DropDown", items, 0);
            
```


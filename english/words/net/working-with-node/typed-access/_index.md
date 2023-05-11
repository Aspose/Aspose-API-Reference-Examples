---
title: Typed Access
linktitle: Typed Access
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-node/typed-access/
---




```csharp
	Document doc = new Document();

	Section section = doc.FirstSection;
	Body body = section.Body;
	
	// Quick typed access to all Table child nodes contained in the Body.
	TableCollection tables = body.Tables;

	foreach (Table table in tables)
	{
		// Quick typed access to the first row of the table.
		table.FirstRow?.Remove();

		// Quick typed access to the last row of the table.
		table.LastRow?.Remove();
	}
            
```


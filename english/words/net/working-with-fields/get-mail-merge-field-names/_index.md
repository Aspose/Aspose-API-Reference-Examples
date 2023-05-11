---
title: Get Mail Merge Field Names
linktitle: Get Mail Merge Field Names
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/get-mail-merge-field-names/
---




```csharp
	Document doc = new Document();

	string[] fieldNames = doc.MailMerge.GetFieldNames();
	
	Console.WriteLine("\nDocument have " + fieldNames.Length + " fields.");
```


---
title: Apply Metered License
linktitle: Apply Metered License
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/apply-license/apply-metered-license/
---



To enable metered license of Aspose.Words for .NET, follow these steps:

- Initialize an instance of the [Metered](/words/net/aspose.words/metered/) class.
- Call the [Metered.SetMeteredKey(string, string)](/words/net/aspose.words/metered/setmeteredkey/) method with public and private key.


```csharp
	try
	{
		Metered metered = new Metered();
		metered.SetMeteredKey("*****", "*****");

		Document doc = new Document(MyDir + "Document.docx");

		Console.WriteLine(doc.PageCount);
	}
	catch (Exception e)
	{
		Console.WriteLine("\nThere was an error setting the license: " + e.Message);
	}
```


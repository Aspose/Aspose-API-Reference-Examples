---
title: Read Vba Macros
linktitle: Read Vba Macros
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-vba-macros/read-vba-macros/
---




```csharp
	Document doc = new Document(MyDir + "VBA project.docm");

	if (doc.VbaProject != null)
	{
		foreach (VbaModule module in doc.VbaProject.Modules)
		{
			Console.WriteLine(module.SourceCode);
		}
	}
            
```


---
title: Read Vba Macros
linktitle: Read Vba Macros
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-vba-macros/read-vba-macros/
---
### Sample source code for Read Vba Macros using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

	Document doc = new Document(dataDir + "VBA project.docm");
	if (doc.VbaProject != null)
	{
		foreach (VbaModule module in doc.VbaProject.Modules)
		{
			Console.WriteLine(module.SourceCode);
		}
	}
```
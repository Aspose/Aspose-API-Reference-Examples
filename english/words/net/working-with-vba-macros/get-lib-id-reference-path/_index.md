---
title: Get Lib Id Reference Path
linktitle: Get Lib Id Reference Path
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-vba-macros/get-lib-id-reference-path/
---
### Sample source code for Get Lib Id Reference Path using Aspose.Words for .NET 
```csharp
	private string GetLibIdReferencePath(string libIdReference)
	{
		if (libIdReference != null)
				{
					string[] refParts = libIdReference.Split('#');
					if (refParts.Length > 3)
						return refParts[3];
				}
				return "";
	}
```
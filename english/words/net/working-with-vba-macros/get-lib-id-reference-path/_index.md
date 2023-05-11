---
title: Get Lib Id Reference Path
linktitle: Get Lib Id Reference Path
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-vba-macros/get-lib-id-reference-path/
---




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


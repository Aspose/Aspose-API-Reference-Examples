---
title: Get Lib Id Path
linktitle: Get Lib Id Path
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-vba-macros/get-lib-id-path/
---
### Sample source code for Get Lib Id Path using Aspose.Words for .NET 
```csharp
	private string GetLibIdPath(VbaReference reference)
        {
		switch (reference.Type)
			{
				case VbaReferenceType.Registered:
				case VbaReferenceType.Original:
				case VbaReferenceType.Control:
					return GetLibIdReferencePath(reference.LibId);
				case VbaReferenceType.Project:
					return GetLibIdProjectPath(reference.LibId);
				default:
					throw new ArgumentOutOfRangeException();
			}
		}
```
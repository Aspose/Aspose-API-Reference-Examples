---
title: Remove Broken Ref
linktitle: Remove Broken Ref
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-vba-macros/remove-broken-ref/
---
### Sample source code for Remove Broken Ref using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

	Document doc = new Document(dataDir + "VBA project.docm");
	// Find and remove the reference with some LibId path.
	const string brokenPath = "brokenPath.dll";
	VbaReferenceCollection references = doc.VbaProject.References;
	for (int i = references.Count - 1; i >= 0; i--)
	{
		VbaReference reference = doc.VbaProject.References.ElementAt(i);
		string path = GetLibIdPath(reference);
		if (path == brokenPath)
			references.RemoveAt(i);
	}
	doc.Save(dataDir + "WorkingWithVba.RemoveBrokenRef.docm");
```
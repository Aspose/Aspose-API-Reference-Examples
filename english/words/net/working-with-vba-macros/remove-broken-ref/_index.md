---
title: Remove Broken Ref
linktitle: Remove Broken Ref
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-vba-macros/remove-broken-ref/
---




```csharp
	Document doc = new Document(MyDir + "VBA project.docm");

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

	doc.Save(ArtifactsDir + "WorkingWithVba.RemoveBrokenRef.docm");
            
```


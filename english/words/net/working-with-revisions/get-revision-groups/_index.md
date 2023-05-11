---
title: Get Revision Groups
linktitle: Get Revision Groups
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-revisions/get-revision-groups/
---




```csharp
	Document doc = new Document(MyDir + "Revisions.docx");

	foreach (RevisionGroup group in doc.Revisions.Groups)
	{
		Console.WriteLine("{0}, {1}:", group.Author, group.RevisionType);
		Console.WriteLine(group.Text);
	}
            
```


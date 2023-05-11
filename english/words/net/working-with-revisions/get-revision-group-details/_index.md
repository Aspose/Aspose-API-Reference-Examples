---
title: Get Revision Group Details
linktitle: Get Revision Group Details
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-revisions/get-revision-group-details/
---




```csharp
	Document doc = new Document(MyDir + "Revisions.docx");

	foreach (Revision revision in doc.Revisions)
	{
		string groupText = revision.Group != null
			? "Revision group text: " + revision.Group.Text
			: "Revision has no group";

		Console.WriteLine("Type: " + revision.RevisionType);
		Console.WriteLine("Author: " + revision.Author);
		Console.WriteLine("Date: " + revision.DateTime);
		Console.WriteLine("Revision text: " + revision.ParentNode.ToString(SaveFormat.Text));
		Console.WriteLine(groupText);
	}
            
```


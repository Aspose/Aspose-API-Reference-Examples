---
title: Get Revision Types
linktitle: Get Revision Types
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-revisions/get-revision-types/
---




```csharp
	Document doc = new Document(MyDir + "Revisions.docx");

	ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
	for (int i = 0; i < paragraphs.Count; i++)
	{
		if (paragraphs[i].IsMoveFromRevision)
			Console.WriteLine("The paragraph {0} has been moved (deleted).", i);
		if (paragraphs[i].IsMoveToRevision)
			Console.WriteLine("The paragraph {0} has been moved (inserted).", i);
	}
            
```


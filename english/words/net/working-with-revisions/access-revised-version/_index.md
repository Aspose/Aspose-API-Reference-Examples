---
title: Access Revised Version
linktitle: Access Revised Version
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-revisions/access-revised-version/
---




```csharp
	Document doc = new Document(MyDir + "Revisions.docx");
	doc.UpdateListLabels();

	// Switch to the revised version of the document.
	doc.RevisionsView = RevisionsView.Final;

	foreach (Revision revision in doc.Revisions)
	{
		if (revision.ParentNode.NodeType == NodeType.Paragraph)
		{
			Paragraph paragraph = (Paragraph) revision.ParentNode;
			if (paragraph.IsListItem)
			{
				Console.WriteLine(paragraph.ListLabel.LabelString);
				Console.WriteLine(paragraph.ListFormat.ListLevel);
			}
		}
	}
            
```


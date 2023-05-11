---
title: Enumerate Child Nodes
linktitle: Enumerate Child Nodes
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-node/enumerate-child-nodes/
---




```csharp
	Document doc = new Document();
	Paragraph paragraph = (Paragraph) doc.GetChild(NodeType.Paragraph, 0, true);

	NodeCollection children = paragraph.ChildNodes;
	foreach (Node child in children)
	{
		// A paragraph may contain children of various types such as runs, shapes, and others.
		if (child.NodeType == NodeType.Run)
		{
			Run run = (Run) child;
			Console.WriteLine(run.Text);
		}
	}
            
```


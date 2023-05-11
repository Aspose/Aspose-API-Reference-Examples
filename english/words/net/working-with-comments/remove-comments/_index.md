---
title: Remove Comments
linktitle: Remove Comments
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-comments/remove-comments/
---




```csharp
	void RemoveComments(Document doc)
	{
		NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

		comments.Clear();
	}
```

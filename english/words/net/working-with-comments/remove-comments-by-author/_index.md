---
title: Remove Comments by Author
linktitle: Remove Comments by Author
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-comments/remove-comments-by-author/
---




```csharp
	void RemoveComments(Document doc, string authorName)
	{
		NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

		// Look through all comments and remove those written by the authorName.
		for (int i = comments.Count - 1; i >= 0; i--)
		{
			Comment comment = (Comment) comments[i];
			if (comment.Author == authorName)
				comment.Remove();
		}
	}
```

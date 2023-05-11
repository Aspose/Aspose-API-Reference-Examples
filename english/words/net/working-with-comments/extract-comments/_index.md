---
title: Extract Comments
linktitle: Extract Comments
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-comments/extract-comments/
---



The following example shows how to extract comments from Document using Aspose.Words for .NET.
- Call [Document.GetChildNodes](/words/net/aspose.words/compositenode/getchildnodes/) method by NodeType.Comment that returns [NodeCollection](/words/net/aspose.words/nodecollection/)
- Iterate the comments to get comment author, datetime and comment text.
 
```csharp
	List<string> ExtractComments(Document doc)
    {
		List<string> collectedComments = new List<string>();
		NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

		foreach (Comment comment in comments)
		{
			collectedComments.Add(comment.Author + " " + comment.DateTime + " " +
								  comment.ToString(SaveFormat.Text));
		}

		return collectedComments;
	}
```

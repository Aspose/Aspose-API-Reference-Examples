---
title: Extract Comments By Author
linktitle: Extract Comments By Author
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-comments/extract-comments-by-author/
---




The following example shows how to extract comments from Document by specific Author using Aspose.Words for .NET.
- Call [Document.GetChildNodes](/words/net/aspose.words/compositenode/getchildnodes/) method by NodeType.Comment that returns [NodeCollection](/words/net/aspose.words/nodecollection/)
- Iterate the comments and check the comment author.
- If comment is by specific author process that comment.

```csharp
	List<string> ExtractComments(Document doc, string authorName)
    {
		List<string> collectedComments = new List<string>();
		NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

		foreach (Comment comment in comments)
		{
			if (comment.Author == authorName)
				collectedComments.Add(comment.Author + " " + comment.DateTime + " " +
									  comment.ToString(SaveFormat.Text));
		}

		return collectedComments;
	}
```

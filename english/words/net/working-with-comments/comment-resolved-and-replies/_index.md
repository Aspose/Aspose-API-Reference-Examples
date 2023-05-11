---
title: Comment Resolved And Replies
linktitle: Comment Resolved And Replies
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-comments/comment-resolved-and-replies/
---




```csharp
	NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

	Comment parentComment = (Comment) comments[0];
	foreach (Comment childComment in parentComment.Replies)
	{
		// Get comment parent and status.
		Console.WriteLine(childComment.Ancestor.Id);
		Console.WriteLine(childComment.Done);

		// And update comment Done mark.
		childComment.Done = true;
	}
```


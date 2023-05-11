---
title: Add Remove Comment Reply
linktitle: Add Remove Comment Reply
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-comments/add-remove-comment-reply/
---



To remove comments reply from a Word Document using Aspose.Words for .NET follow these steps.
- Create an instance of the [Document](/words/net/aspose.words/document/) class.
- Get [Comment](/words/net/aspose.words/comment/) object by calling [Document.GetChild](/words/net/aspose.words/compositenode/getchild/) method.
- Invoke [Comment.RemoveReply](/words/net/aspose.words/comment/removereply/) method with the target reply to remove.
- Save the document. 
```csharp
            
	Document doc = new Document(MyDir + "Comments.docx");

	Comment comment = (Comment) doc.GetChild(NodeType.Comment, 0, true);
	comment.RemoveReply(comment.Replies[0]);

	comment.AddReply("John Doe", "JD", new DateTime(2017, 9, 25, 12, 15, 0), "New reply");

	doc.Save(ArtifactsDir + "WorkingWithComments.AddRemoveCommentReply.docx");
            
```


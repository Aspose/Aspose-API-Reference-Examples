---
title: Process Comments
linktitle: Process Comments
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-comments/process-comments/
---




```csharp
            
	Document doc = new Document(MyDir + "Comments.docx");

	// Extract the information about the comments of all the authors.
	foreach (string comment in ExtractComments(doc))
		Console.Write(comment);

	// Remove comments by the "pm" author.
	RemoveComments(doc, "pm");
	Console.WriteLine("Comments from \"pm\" are removed!");

	// Extract the information about the comments of the "ks" author.
	foreach (string comment in ExtractComments(doc, "ks"))
		Console.Write(comment);

	// Read the comment's reply and resolve them.
	CommentResolvedAndReplies(doc);

	// Remove all comments.
	RemoveComments(doc);
	Console.WriteLine("All comments are removed!");

	doc.Save(ArtifactsDir + "WorkingWithComments.ProcessComments.docx");
            
```




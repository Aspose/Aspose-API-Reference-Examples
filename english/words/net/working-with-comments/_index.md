---
title: Working with Comments
linktitle: Working with Comments
second_title: Aspose.Words for .NET API Reference
description: Examples show how to add comments, anchor comments, add/remove comment reply, extract comments, and resolve comments and replies in Aspose.Words for .NET
type: docs
weight: 50
url: /words/net/working-with-comments/
---

The following examples show how to add comments, anchor comments, add/remove comment reply, extract comments, and resolve comments and replies using [Comment](/words/net/aspose.words/comment/) class in Aspose.Words for .NET.

## Add Comments
To add comments into a Word Document using Aspose.Words for .NET follow these steps.
- Create an instance of the [Document](/words/net/aspose.words/document/) class.
- Create an instance of the [DocumentBuilder](/words/net/aspose.words/documentbuilder/) with Document object.
- Initiate [Comment](/words/net/aspose.words/comment/) [instance](/words/net/aspose.words/comment/comment/#constructor_1) with Document object, author name, author initials and datetime.
- Add comment object using [AppendChild](/words/net/aspose.words/compositenode/appendchild/) method of [DocumentBuilder.CurrentParagraph](/words/net/aspose.words/documentbuilder/currentparagraph/).
- Add new [Paragraph](/words/net/aspose.words/paragraph/) in Paragraphs collection of comment object.
- Add new [Run](/words/net/aspose.words/run/) in [Runs](/words/net/aspose.words/paragraph/runs/) collection of FirstParagraph of comment object.
- Save the document.    

```csharp

	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	builder.Write("Some text is added.");
	Comment comment = new Comment(doc, "Awais Hafeez", "AH", DateTime.Today);

	builder.CurrentParagraph.AppendChild(comment);

	comment.Paragraphs.Add(new Paragraph(doc));
	comment.FirstParagraph.Runs.Add(new Run(doc, "Comment text."));

	doc.Save(ArtifactsDir + "WorkingWithComments.AddComments.docx");
            
```

## Anchor Comment
To anchor comments into a Word Document using Aspose.Words for .NET follow these steps.
- Create an instance of the [Document](/words/net/aspose.words/document/) class.
- Create three [Run](/words/net/aspose.words/run/) objects.
- The first two run some text, while the third runs a [Comment](/words/net/aspose.words/comment/).
- Each of the Run objects has an associated CommentRangeStart and CommentRangeEnd object.
- The example then creates two Paragraph objects and appends them to the document's FirstSection.Body node.
- The first Paragraph object contains content for the first run, while the second Paragraph object contains content for the second run.
- Finally, the example creates a Comment object and attaches it to the document's FirstParagraph node.
- The Comment object contains information about both runs (the text and comment).
- The example creates a document with two sections, the first of which has a paragraph and the second of which has a comment.
- The example then creates two runs, one for the paragraph and one for the comment.
- Finally, it inserts the comments into their respective positions in the document.
- When executed, this example will create a document that looks like this: Some text is added is added to the first section.
- A Comment text.
- Save the document.
```csharp
            
	Document doc = new Document();

	Paragraph para1 = new Paragraph(doc);
	Run run1 = new Run(doc, "Some ");
	Run run2 = new Run(doc, "text ");
	para1.AppendChild(run1);
	para1.AppendChild(run2);
	doc.FirstSection.Body.AppendChild(para1);

	Paragraph para2 = new Paragraph(doc);
	Run run3 = new Run(doc, "is ");
	Run run4 = new Run(doc, "added ");
	para2.AppendChild(run3);
	para2.AppendChild(run4);
	doc.FirstSection.Body.AppendChild(para2);

	Comment comment = new Comment(doc, "Awais Hafeez", "AH", DateTime.Today);
	comment.Paragraphs.Add(new Paragraph(doc));
	comment.FirstParagraph.Runs.Add(new Run(doc, "Comment text."));

	CommentRangeStart commentRangeStart = new CommentRangeStart(doc, comment.Id);
	CommentRangeEnd commentRangeEnd = new CommentRangeEnd(doc, comment.Id);

	run1.ParentNode.InsertAfter(commentRangeStart, run1);
	run3.ParentNode.InsertAfter(commentRangeEnd, run3);
	commentRangeEnd.ParentNode.InsertAfter(comment, commentRangeEnd);

	doc.Save(ArtifactsDir + "WorkingWithComments.AnchorComment.doc");
            
```

## Add Remove Comment Reply
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

## Extract Comments
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
## Extract Comments By Author

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
## Remove Comments

```csharp
	void RemoveComments(Document doc)
	{
		NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

		comments.Clear();
	}
```
## Remove Comments by Author

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
## Process Comments

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



## Comment Resolved And Replies

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


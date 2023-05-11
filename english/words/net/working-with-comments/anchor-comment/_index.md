---
title: Anchor Comment
linktitle: Anchor Comment
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-comments/anchor-comment/
---



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
- When executed, this tutorial will create a document that looks like this: Some text is added is added to the first section.
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


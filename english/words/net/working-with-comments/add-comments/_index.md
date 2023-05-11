---
title: Add Comments
linktitle: Add Comments
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-comments/add-comments/
---



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


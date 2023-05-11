---
title: Accept Revisions
linktitle: Accept Revisions
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-revisions/accept-revisions/
---




```csharp
	Document doc = new Document();
	Body body = doc.FirstSection.Body;
	Paragraph para = body.FirstParagraph;

	// Add text to the first paragraph, then add two more paragraphs.
	para.AppendChild(new Run(doc, "Paragraph 1. "));
	body.AppendParagraph("Paragraph 2. ");
	body.AppendParagraph("Paragraph 3. ");

	// We have three paragraphs, none of which registered as any type of revision
	// If we add/remove any content in the document while tracking revisions,
	// they will be displayed as such in the document and can be accepted/rejected.
	doc.StartTrackRevisions("John Doe", DateTime.Now);

	// This paragraph is a revision and will have the according "IsInsertRevision" flag set.
	para = body.AppendParagraph("Paragraph 4. ");
	Assert.True(para.IsInsertRevision);

	// Get the document's paragraph collection and remove a paragraph.
	ParagraphCollection paragraphs = body.Paragraphs;
	Assert.AreEqual(4, paragraphs.Count);
	para = paragraphs[2];
	para.Remove();

	// Since we are tracking revisions, the paragraph still exists in the document, will have the "IsDeleteRevision" set
	// and will be displayed as a revision in Microsoft Word, until we accept or reject all revisions.
	Assert.AreEqual(4, paragraphs.Count);
	Assert.True(para.IsDeleteRevision);

	// The delete revision paragraph is removed once we accept changes.
	doc.AcceptAllRevisions();
	Assert.AreEqual(3, paragraphs.Count);
	Assert.That(para, Is.Empty);

	// Stopping the tracking of revisions makes this text appear as normal text.
	// Revisions are not counted when the document is changed.
	doc.StopTrackRevisions();

	// Save the document.
	doc.Save(ArtifactsDir + "WorkingWithRevisions.AcceptRevisions.docx");
            
```


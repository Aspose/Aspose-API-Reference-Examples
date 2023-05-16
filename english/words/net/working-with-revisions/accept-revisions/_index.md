---
title: Accept Revisions
linktitle: Accept Revisions
second_title: Aspose.Words for .NET API Reference
description: Acceptez les modifications dans un document Word avec Aspose.Words pour .NET. Code source inclus. Sortie formatée en markdown.
type: docs
weight: 10
url: /words/net/working-with-revisions/accept-revisions/
---

In this step-by-step guide, we'll walk you through how to accept changes in a Word document using Aspose.Words for .NET. We'll provide you with the complete source code and show you how to format the markdown output.

## Step 1: Creating the document

The first step is to create a new document.

```csharp
Document doc = new Document();
```

## Step 2: Add paragraphs

Next, we will add paragraphs to the document.

```csharp
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

// Add text to the first paragraph, then add two more paragraphs.
para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2.");
body.AppendParagraph("Paragraph 3.");
```

## Step 3: Track revisions

We are going to enable revision tracking in the document.

```csharp
doc.StartTrackRevisions("John Doe", DateTime.Now);
```

## Step 4: Adding a paragraph as a review

We will add a new paragraph which will be considered a revision.

```csharp
para = body.AppendParagraph("Paragraph 4.");
```

## Step 5: Delete a paragraph

We are going to delete an existing paragraph from the document.

```csharp
ParagraphCollection paragraphs = body.Paragraphs;
para = paragraphs[2];
para.Remove();
```

## Step 6: Accept Changes

We will now accept all the changes made to the document.

```csharp
doc.AcceptAllRevisions();
```

## Step 7: Stop Tracking Reviews

Finally, we'll stop tracking revisions in the document.

```csharp
doc.StopTrackRevisions();
```

## Markdown output formats

The document output can be formatted in markdown to improve readability. For example :

```markdown
- Paragraph 1.
- Paragraph 2.
- Paragraph 3.
```

### Example source code for Accept Revisions using Aspose.Words for .NET

Here is the complete source code for accepting changes in a document using Aspose.Words for .NET:

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

// Add text to the first paragraph, then add two more paragraphs.
para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2.");
body.AppendParagraph("Paragraph 3.");

// Start tracking revisions.
doc.StartTrackRevisions("John Doe", DateTime.Now);

// Add a revision paragraph.
para = body.AppendParagraph("Paragraph 4.");

// Get the document's paragraph collection and remove a paragraph.
ParagraphCollection paragraphs = body.Paragraphs;
para = paragraphs[2];
para.Remove();

// Accept all revisions.
doc.AcceptAllRevisions();

// Stop tracking revisions.
doc.StopTrackRevisions();

// Save the document.
doc.Save(ArtifactsDir + "WorkingWithRevisions.AcceptRevisions.docx");
```


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


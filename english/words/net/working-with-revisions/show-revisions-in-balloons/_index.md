---
title: Show Revisions In Balloons
linktitle: Show Revisions In Balloons
second_title: Aspose.Words for .NET API Reference
description: Display revisions in balloons with Aspose.Words for .NET.
type: docs
weight: 10
url: /words/net/working-with-revisions/show-revisions-in-balloons/
---

In this step-by-step guide, we are going to show you how to show revisions in balloons in a Word document using Aspose.Words for .NET. We'll provide you with the complete source code and show you how to format the markdown output.

## Step 1: Loading the document

The first step is to upload the document containing the revisions.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
```

## Step 2: Configure review display options

We will configure the display options to make revisions visible in balloons.

```csharp
doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
doc.LayoutOptions.RevisionOptions.MeasurementUnit = MeasurementUnits.Inches;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;
```

## Step 3: Save the document in PDF format

Finally, we'll save the document as a PDF with the revisions displayed in balloons.

```csharp
doc.Save(ArtifactsDir + "WorkingWithRevisions.ShowRevisionsInBalloons.pdf");
```

## Markdown output formats

The output can be formatted in markdown to improve readability. For example :

```markdown
- Revisions are displayed in bubbles with revision bars on the right side.
```

### Example source code for Show Revisions In Balloons using Aspose.Words for .NET

Here is the complete source code to show revisions in balloons in a document using Aspose.Words for .NET:

```csharp
                       
	Document doc = new Document(MyDir + "Revisions.docx");

	// Renders insert revisions inline, delete and format revisions in balloons.
	doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
	doc.LayoutOptions.RevisionOptions.MeasurementUnit = MeasurementUnits.Inches;
	// Renders revision bars on the right side of a page.
	doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;
	
	doc.Save(ArtifactsDir + "WorkingWithRevisions.ShowRevisionsInBalloons.pdf");
	
```





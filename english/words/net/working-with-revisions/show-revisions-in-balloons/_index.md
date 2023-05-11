---
title: Show Revisions In Balloons
linktitle: Show Revisions In Balloons
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-revisions/show-revisions-in-balloons/
---




```csharp
                       
	Document doc = new Document(MyDir + "Revisions.docx");

	// Renders insert revisions inline, delete and format revisions in balloons.
	doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
	doc.LayoutOptions.RevisionOptions.MeasurementUnit = MeasurementUnits.Inches;
	// Renders revision bars on the right side of a page.
	doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;
	
	doc.Save(ArtifactsDir + "WorkingWithRevisions.ShowRevisionsInBalloons.pdf");
	
```


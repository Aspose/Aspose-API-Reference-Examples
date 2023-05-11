---
title: Remove Comments In Pdf
linktitle: Remove Comments In Pdf
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-revisions/remove-comments-in-pdf/
---




```csharp
	Document doc = new Document(MyDir + "Revisions.docx");

	// Do not render the comments in PDF.
	doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.Hide;

	doc.Save(ArtifactsDir + "WorkingWithRevisions.RemoveCommentsInPdf.pdf");
            
```


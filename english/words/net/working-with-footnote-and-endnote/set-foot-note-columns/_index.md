---
title: Set Foot Note Columns
linktitle: Set Foot Note Columns
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-footnote-and-endnote/set-foot-note-columns/
---




```csharp
            
	Document doc = new Document(MyDir + "Document.docx");

	// Specify the number of columns with which the footnotes area is formatted.
	doc.FootnoteOptions.Columns = 3;
	
	doc.Save(ArtifactsDir + "WorkingWithFootnotes.SetFootNoteColumns.docx");
            
```


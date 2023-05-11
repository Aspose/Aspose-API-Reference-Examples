---
title: Set Footnote And End Note Position
linktitle: Set Footnote And End Note Position
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-footnote-and-endnote/set-footnote-and-end-note-position/
---




```csharp
            
	Document doc = new Document(MyDir + "Document.docx");

	doc.FootnoteOptions.Position = FootnotePosition.BeneathText;
	doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;
	
	doc.Save(ArtifactsDir + "WorkingWithFootnotes.SetFootnoteAndEndNotePosition.docx");
            
```


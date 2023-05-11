---
title: Set Endnote Options
linktitle: Set Endnote Options
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-footnote-and-endnote/set-endnote-options/
---




```csharp
            
	Document doc = new Document(MyDir + "Document.docx");
	DocumentBuilder builder = new DocumentBuilder(doc);
	
	builder.Write("Some text");
	builder.InsertFootnote(FootnoteType.Endnote, "Footnote text.");

	EndnoteOptions option = doc.EndnoteOptions;
	option.RestartRule = FootnoteNumberingRule.RestartPage;
	option.Position = EndnotePosition.EndOfSection;

	doc.Save(ArtifactsDir + "WorkingWithFootnotes.SetEndnoteOptions.docx");
            
```


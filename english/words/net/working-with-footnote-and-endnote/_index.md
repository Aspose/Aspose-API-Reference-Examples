---
title: Working with Footnote and Endnote
linktitle: Working with Footnote and Endnote
second_title: Aspose.Words for .NET API Reference
description: Tutorials explain how to set Foot note and end note in Word Document using Aspose.Words for .NET
type: docs
weight: 660
url: /words/net/working-with-footnote-and-endnote/
---
The following tutorials explain how to set Foot note and end note in Word Document using Aspose.Words for .NET.

## Set Foot Note Columns

```csharp
            
	Document doc = new Document(MyDir + "Document.docx");

	// Specify the number of columns with which the footnotes area is formatted.
	doc.FootnoteOptions.Columns = 3;
	
	doc.Save(ArtifactsDir + "WorkingWithFootnotes.SetFootNoteColumns.docx");
            
```

## Set Footnote And End Note Position

```csharp
            
	Document doc = new Document(MyDir + "Document.docx");

	doc.FootnoteOptions.Position = FootnotePosition.BeneathText;
	doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;
	
	doc.Save(ArtifactsDir + "WorkingWithFootnotes.SetFootnoteAndEndNotePosition.docx");
            
```

## Set Endnote Options

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


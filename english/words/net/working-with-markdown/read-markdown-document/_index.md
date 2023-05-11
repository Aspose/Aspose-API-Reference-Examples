---
title: Read Markdown Document
linktitle: Read Markdown Document
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-markdown/read-markdown-document/
---




```csharp
	Document doc = new Document(MyDir + "Quotes.md");

	// Let's remove Heading formatting from a Quote in the very last paragraph.
	Paragraph paragraph = doc.FirstSection.Body.LastParagraph;
	paragraph.ParagraphFormat.Style = doc.Styles["Quote"];

	doc.Save(ArtifactsDir + "WorkingWithMarkdown.ReadMarkdownDocument.md");
            
```


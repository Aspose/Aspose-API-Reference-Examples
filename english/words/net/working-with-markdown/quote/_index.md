---
title: Quote
linktitle: Quote
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-markdown/quote/
---




```csharp
	// Use a document builder to add content to the document.
	DocumentBuilder builder = new DocumentBuilder();

	// By default a document stores blockquote style for the first level.
	builder.ParagraphFormat.StyleName = "Quote";
	builder.Writeln("Blockquote");

	// Create styles for nested levels through style inheritance.
	Style quoteLevel2 = builder.Document.Styles.Add(StyleType.Paragraph, "Quote1");
	builder.ParagraphFormat.Style = quoteLevel2;
	builder.Document.Styles["Quote1"].BaseStyleName = "Quote";
	builder.Writeln("1. Nested blockquote");
            
```


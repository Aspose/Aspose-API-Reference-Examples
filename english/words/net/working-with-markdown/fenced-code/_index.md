---
title: Fenced Code
linktitle: Fenced Code
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-markdown/fenced-code/
---




```csharp
	// Use a document builder to add content to the document.
	DocumentBuilder builder = new DocumentBuilder();

	Style fencedCode = builder.Document.Styles.Add(StyleType.Paragraph, "FencedCode");
	builder.ParagraphFormat.Style = fencedCode;
	builder.Writeln("This is an fenced code");

	Style fencedCodeWithInfo = builder.Document.Styles.Add(StyleType.Paragraph, "FencedCode.C#");
	builder.ParagraphFormat.Style = fencedCodeWithInfo;
	builder.Writeln("This is a fenced code with info string");
            
```


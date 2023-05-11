---
title: Indented Code
linktitle: Indented Code
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-markdown/indented-code/
---




```csharp
	// Use a document builder to add content to the document.
	DocumentBuilder builder = new DocumentBuilder();

	Style indentedCode = builder.Document.Styles.Add(StyleType.Paragraph, "IndentedCode");
	builder.ParagraphFormat.Style = indentedCode;
	builder.Writeln("This is an indented code");
            
```


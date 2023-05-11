---
title: Heading
linktitle: Heading
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-markdown/heading/
---




```csharp
	// Use a document builder to add content to the document.
	DocumentBuilder builder = new DocumentBuilder();

	// By default Heading styles in Word may have Bold and Italic formatting.
	//If we do not want to be emphasized, set these properties explicitly to false.
	builder.Font.Bold = false;
	builder.Font.Italic = false;

	builder.ParagraphFormat.StyleName = "Heading 1";
	builder.Writeln("This is an H1 tag");
            
```


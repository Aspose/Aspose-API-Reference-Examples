---
title: Inline Code
linktitle: Inline Code
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-markdown/inline-code/
---




```csharp
	// Use a document builder to add content to the document.
	DocumentBuilder builder = new DocumentBuilder();

	// Number of backticks is missed, one backtick will be used by default.
	Style inlineCode1BackTicks = builder.Document.Styles.Add(StyleType.Character, "InlineCode");
	builder.Font.Style = inlineCode1BackTicks;
	builder.Writeln("Text with InlineCode style with 1 backtick");

	// There will be 3 backticks.
	Style inlineCode3BackTicks = builder.Document.Styles.Add(StyleType.Character, "InlineCode.3");
	builder.Font.Style = inlineCode3BackTicks;
	builder.Writeln("Text with InlineCode style with 3 backtick");
            
```


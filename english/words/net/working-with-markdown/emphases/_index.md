---
title: Emphases
linktitle: Emphases
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-markdown/emphases/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	builder.Writeln("Markdown treats asterisks (*) and underscores (_) as indicators of emphasis.");
	builder.Write("You can write ");

	builder.Font.Bold = true;
	builder.Write("bold");

	builder.Font.Bold = false;
	builder.Write(" or ");

	builder.Font.Italic = true;
	builder.Write("italic");

	builder.Font.Italic = false;
	builder.Writeln(" text. ");

	builder.Write("You can also write ");
	builder.Font.Bold = true;

	builder.Font.Italic = true;
	builder.Write("BoldItalic");

	builder.Font.Bold = false;
	builder.Font.Italic = false;
	builder.Write("text.");

	builder.Document.Save(ArtifactsDir + "WorkingWithMarkdown.Emphases.md");
            
```


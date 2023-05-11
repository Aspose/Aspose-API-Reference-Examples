---
title: Specify Locale At Field Level
linktitle: Specify Locale At Field Level
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/specify-locale-at-field-level/
---




```csharp
	DocumentBuilder builder = new DocumentBuilder();

	Field field = builder.InsertField(FieldType.FieldDate, true);
	field.LocaleId = 1049;
	
	builder.Document.Save(ArtifactsDir + "WorkingWithFields.SpecifylocaleAtFieldlevel.docx");
```


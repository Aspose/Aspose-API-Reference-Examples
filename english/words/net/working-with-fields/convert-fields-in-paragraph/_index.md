---
title: Convert Fields In Paragraph
linktitle: Convert Fields In Paragraph
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/convert-fields-in-paragraph/
---




```csharp
	Document doc = new Document(MyDir + "Linked fields.docx");

	// Pass the appropriate parameters to convert all IF fields to text that are encountered only in the last 
	// paragraph of the document.
	doc.FirstSection.Body.LastParagraph.Range.Fields.Where(f => f.Type == FieldType.FieldIf).ToList()
		.ForEach(f => f.Unlink());

	doc.Save(ArtifactsDir + "WorkingWithFields.TestFile.docx");
```


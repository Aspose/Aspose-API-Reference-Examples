---
title: Convert Fields In Document
linktitle: Convert Fields In Document
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/convert-fields-in-document/
---




```csharp
	Document doc = new Document(MyDir + "Linked fields.docx");

	// Pass the appropriate parameters to convert all IF fields encountered in the document (including headers and footers) to text.
	doc.Range.Fields.Where(f => f.Type == FieldType.FieldIf).ToList().ForEach(f => f.Unlink());

	// Save the document with fields transformed to disk
	doc.Save(ArtifactsDir + "WorkingWithFields.ConvertFieldsInDocument.docx");
	
```


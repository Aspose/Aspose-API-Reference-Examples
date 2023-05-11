---
title: Rename Merge Fields
linktitle: Rename Merge Fields
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/rename-merge-fields/
---




```csharp  
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
	builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

	foreach (Field f in doc.Range.Fields)
	{
		if (f.Type == FieldType.FieldMergeField)
		{
			FieldMergeField mergeField = (FieldMergeField)f;
			mergeField.FieldName = mergeField.FieldName + "_Renamed";
			mergeField.Update();
		}
	}

	doc.Save(ArtifactsDir + "WorkingWithFields.RenameMergeFields.docx");
```


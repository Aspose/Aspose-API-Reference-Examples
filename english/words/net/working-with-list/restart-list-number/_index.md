---
title: Restart List Number
linktitle: Restart List Number
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-list/restart-list-number/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	// Create a list based on a template.
	List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
	list1.ListLevels[0].Font.Color = Color.Red;
	list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

	builder.Writeln("List 1 starts below:");
	builder.ListFormat.List = list1;
	builder.Writeln("Item 1");
	builder.Writeln("Item 2");
	builder.ListFormat.RemoveNumbers();

	// To reuse the first list, we need to restart numbering by creating a copy of the original list formatting.
	List list2 = doc.Lists.AddCopy(list1);

	// We can modify the new list in any way, including setting a new start number.
	list2.ListLevels[0].StartAt = 10;

	builder.Writeln("List 2 starts below:");
	builder.ListFormat.List = list2;
	builder.Writeln("Item 1");
	builder.Writeln("Item 2");
	builder.ListFormat.RemoveNumbers();

	builder.Document.Save(ArtifactsDir + "WorkingWithList.RestartListNumber.docx");
            
```


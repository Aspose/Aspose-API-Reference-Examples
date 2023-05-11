---
title: Specify List Level
linktitle: Specify List Level
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-list/specify-list-level/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	// Create a numbered list based on one of the Microsoft Word list templates
	// and apply it to the document builder's current paragraph.
	builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberArabicDot);

	// There are nine levels in this list, let's try them all.
	for (int i = 0; i < 9; i++)
	{
		builder.ListFormat.ListLevelNumber = i;
		builder.Writeln("Level " + i);
	}

	// Create a bulleted list based on one of the Microsoft Word list templates
	// and apply it to the document builder's current paragraph.
	builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDiamonds);

	for (int i = 0; i < 9; i++)
	{
		builder.ListFormat.ListLevelNumber = i;
		builder.Writeln("Level " + i);
	}

	// This is a way to stop list formatting.
	builder.ListFormat.List = null;

	builder.Document.Save(ArtifactsDir + "WorkingWithList.SpecifyListLevel.docx");
            
```


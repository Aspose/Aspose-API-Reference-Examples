---
title: Restart List At Each Section
linktitle: Restart List At Each Section
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-list/restart-list-at-each-section/
---




```csharp
	Document doc = new Document();
	
	doc.Lists.Add(ListTemplate.NumberDefault);

	List list = doc.Lists[0];
	list.IsRestartAtEachSection = true;

	DocumentBuilder builder = new DocumentBuilder(doc);
	builder.ListFormat.List = list;

	for (int i = 1; i < 45; i++)
	{
		builder.Writeln($"List Item {i}");

		if (i == 15)
			builder.InsertBreak(BreakType.SectionBreakNewPage);
	}

	// IsRestartAtEachSection will be written only if compliance is higher then OoxmlComplianceCore.Ecma376.
	OoxmlSaveOptions options = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Transitional };

	doc.Save(ArtifactsDir + "WorkingWithList.RestartListAtEachSection.docx", options);
            
```


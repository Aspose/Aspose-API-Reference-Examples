---
title: Modify Page Setup In All Sections
linktitle: Modify Page Setup In All Sections
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-section/modify-page-setup-in-all-sections/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	builder.Writeln("Hello1");
	doc.AppendChild(new Section(doc));
	builder.Writeln("Hello22");
	doc.AppendChild(new Section(doc));
	builder.Writeln("Hello3");
	doc.AppendChild(new Section(doc));
	builder.Writeln("Hello45");

	// It is important to understand that a document can contain many sections,
	// and each section has its page setup. In this case, we want to modify them all.
	foreach (Section section in doc)
		section.PageSetup.PaperSize = PaperSize.Letter;

	doc.Save(ArtifactsDir + "WorkingWithSection.ModifyPageSetupInAllSections.doc");
            
```


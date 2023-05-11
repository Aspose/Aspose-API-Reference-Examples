---
title: Change Locale
linktitle: Change Locale
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/change-locale/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	builder.InsertField("MERGEFIELD Date");

	// Store the current culture so it can be set back once mail merge is complete.
	CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
	// Set to German language so dates and numbers are formatted using this culture during mail merge.
	Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");

	doc.MailMerge.Execute(new[] { "Date" }, new object[] { DateTime.Now });
	
	Thread.CurrentThread.CurrentCulture = currentCulture;
	
	doc.Save(ArtifactsDir + "WorkingWithFields.ChangeLocale.docx");

```


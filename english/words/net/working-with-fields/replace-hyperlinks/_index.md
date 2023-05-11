---
title: Replace Hyperlinks
linktitle: Replace Hyperlinks
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/replace-hyperlinks/
---




```csharp
	Document doc = new Document(MyDir + "Hyperlinks.docx");

	foreach (Field field in doc.Range.Fields)
	{
		if (field.Type == FieldType.FieldHyperlink)
		{
			FieldHyperlink hyperlink = (FieldHyperlink) field;

			// Some hyperlinks can be local (links to bookmarks inside the document), ignore these.
			if (hyperlink.SubAddress != null)
				continue;

			hyperlink.Address = "http://www.aspose.com";
			hyperlink.Result = "Aspose - The .NET & Java Component Publisher";
		}
	}

	doc.Save(ArtifactsDir + "WorkingWithFields.ReplaceHyperlinks.docx");
```


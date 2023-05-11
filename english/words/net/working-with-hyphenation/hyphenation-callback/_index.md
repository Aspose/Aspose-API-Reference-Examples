---
title: Hyphenation Callback
linktitle: Hyphenation Callback
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-hyphenation/hyphenation-callback/
---




```csharp
	try
	{
		// Register hyphenation callback.
		Hyphenation.Callback = new CustomHyphenationCallback();

		Document document = new Document(MyDir + "German text.docx");
		document.Save(ArtifactsDir + "WorkingWithHyphenation.HyphenationCallback.pdf");
	}
	catch (Exception e) when (e.Message.StartsWith("Missing hyphenation dictionary"))
	{
		Console.WriteLine(e.Message);
	}
	finally
	{
		Hyphenation.Callback = null;
	}
```


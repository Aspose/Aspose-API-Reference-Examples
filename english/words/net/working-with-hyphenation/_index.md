---
title: Working with Hyphenation
linktitle: Working with Hyphenation
second_title: Aspose.Words for .NET API Reference
description: Examples contains hyphenate Words of Languages, load hyphenation dictionary for language and hyphenation callback using Aspose.Words for .NET.
type: docs
weight: 750
url: /words/net/working-with-hyphenation/
---

The following examples contains hyphenate Words of Languages, load hyphenation dictionary for language and hyphenation callback using Aspose.Words for .NET.

## Hyphenate Words Of Languages

```csharp
	Document doc = new Document(MyDir + "German text.docx");

	Hyphenation.RegisterDictionary("en-US", MyDir + "hyph_en_US.dic");
	Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

	doc.Save(ArtifactsDir + "WorkingWithHyphenation.HyphenateWordsOfLanguages.pdf");    
```

## Load Hyphenation Dictionary For Language

```csharp
	Document doc = new Document(MyDir + "German text.docx");
	
	Stream stream = File.OpenRead(MyDir + "hyph_de_CH.dic");
	Hyphenation.RegisterDictionary("de-CH", stream);

	doc.Save(ArtifactsDir + "WorkingWithHyphenation.LoadHyphenationDictionaryForLanguage.pdf");  
```

## Hyphenation Callback

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


---
title: Load Hyphenation Dictionary For Language
linktitle: Load Hyphenation Dictionary For Language
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-hyphenation/load-hyphenation-dictionary-for-language/
---




```csharp
	Document doc = new Document(MyDir + "German text.docx");
	
	Stream stream = File.OpenRead(MyDir + "hyph_de_CH.dic");
	Hyphenation.RegisterDictionary("de-CH", stream);

	doc.Save(ArtifactsDir + "WorkingWithHyphenation.LoadHyphenationDictionaryForLanguage.pdf");  
```


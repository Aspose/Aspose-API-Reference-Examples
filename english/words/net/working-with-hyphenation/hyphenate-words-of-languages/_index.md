---
title: Hyphenate Words Of Languages
linktitle: Hyphenate Words Of Languages
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-hyphenation/hyphenate-words-of-languages/
---




```csharp
	Document doc = new Document(MyDir + "German text.docx");

	Hyphenation.RegisterDictionary("en-US", MyDir + "hyph_en_US.dic");
	Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

	doc.Save(ArtifactsDir + "WorkingWithHyphenation.HyphenateWordsOfLanguages.pdf");    
```


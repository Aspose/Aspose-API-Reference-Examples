---
title: Open Type Features
linktitle: Open Type Features
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/enable-opentype-features/open-type-features/
---




To enable OpenType features follow the these steps. 
- Create an instance of the [Document](/words/net/aspose.words/document/) class.
- Set [Document.LayoutOptions](/words/net/aspose.words/document/layoutoptions/)'s propery [LayoutOptions.TextShaperFactory](/words/net/aspose.words.layout/layoutoptions/textshaperfactory/) 
```csharp
	Document doc = new Document(MyDir + "OpenType text shaping.docx");

	// When we set the text shaper factory, the layout starts to use OpenType features.
	// An Instance property returns BasicTextShaperCache object wrapping HarfBuzzTextShaperFactory.
	doc.LayoutOptions.TextShaperFactory = Aspose.Words.Shaping.HarfBuzz.HarfBuzzTextShaperFactory.Instance;

	doc.Save(ArtifactsDir + "WorkingWithHarfBuzz.OpenTypeFeatures.pdf");
```


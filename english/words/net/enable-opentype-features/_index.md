---
title: Enable OpenType features
linktitle: Enable OpenType features
second_title: Aspose.Words for .NET API Reference
description: Example shows how to enable OpenType features in Aspose.Words for .NET
type: docs
weight: 40
url: /words/net/enable-opentype-features/
---

The following example shows how to enable OpenType features in Aspose.Words for .NET.

## Open Type Features

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


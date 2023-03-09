---
title: Enable OpenType features
linktitle: Enable OpenType features
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 40
url: /words/net/enable-opentype-features/
---

## Open Type Features

```csharp
        {
            //ExStart:OpenTypeFeatures
            Document doc = new Document(MyDir + "OpenType text shaping.docx");

            // When we set the text shaper factory, the layout starts to use OpenType features.
            // An Instance property returns BasicTextShaperCache object wrapping HarfBuzzTextShaperFactory.
            doc.LayoutOptions.TextShaperFactory = Aspose.Words.Shaping.HarfBuzz.HarfBuzzTextShaperFactory.Instance;

            doc.Save(ArtifactsDir + "WorkingWithHarfBuzz.OpenTypeFeatures.pdf");
            //ExEnd:OpenTypeFeatures
        }

```


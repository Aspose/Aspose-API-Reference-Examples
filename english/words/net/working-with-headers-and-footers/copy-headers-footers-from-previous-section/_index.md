---
title: Copy Headers Footers From Previous Section
linktitle: Copy Headers Footers From Previous Section
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-headers-and-footers/copy-headers-footers-from-previous-section/
---




```csharp
	Section previousSection = (Section)section.PreviousSibling;

	if (previousSection == null)
		return;

	section.HeadersFooters.Clear();

	foreach (HeaderFooter headerFooter in previousSection.HeadersFooters)
		section.HeadersFooters.Add(headerFooter.Clone(true));
```


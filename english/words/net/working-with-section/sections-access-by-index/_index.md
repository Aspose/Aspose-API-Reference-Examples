---
title: Sections Access By Index
linktitle: Sections Access By Index
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-section/sections-access-by-index/
---




```csharp
	Document doc = new Document(MyDir + "Document.docx");
	
	Section section = doc.Sections[0];
	section.PageSetup.LeftMargin = 90; // 3.17 cm
	section.PageSetup.RightMargin = 90; // 3.17 cm
	section.PageSetup.TopMargin = 72; // 2.54 cm
	section.PageSetup.BottomMargin = 72; // 2.54 cm
	section.PageSetup.HeaderDistance = 35.4; // 1.25 cm
	section.PageSetup.FooterDistance = 35.4; // 1.25 cm
	section.PageSetup.TextColumns.Spacing = 35.4; // 1.25 cm
            
```


---
title: Delete Section Content
linktitle: Delete Section Content
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-section/delete-section-content/
---




```csharp
	Document doc = new Document(MyDir + "Document.docx");
	
	Section section = doc.Sections[0];
	section.ClearContent();
            
```


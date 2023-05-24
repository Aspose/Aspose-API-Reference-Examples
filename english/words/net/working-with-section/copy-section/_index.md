---
title: Copy Section
linktitle: Copy Section
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-section/copy-section/
---




```csharp
	Document srcDoc = new Document(MyDir + "Document.docx");
	Document dstDoc = new Document();

	Section sourceSection = srcDoc.Sections[0];
	Section newSection = (Section) dstDoc.ImportNode(sourceSection, true);
	dstDoc.Sections.Add(newSection);
	
	dstDoc.Save(ArtifactsDir + "WorkingWithSection.CopySection.docx");
            
```


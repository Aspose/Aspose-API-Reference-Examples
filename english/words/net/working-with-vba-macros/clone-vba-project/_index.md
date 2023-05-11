---
title: Clone Vba Project
linktitle: Clone Vba Project
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-vba-macros/clone-vba-project/
---




```csharp
	Document doc = new Document(MyDir + "VBA project.docm");
	Document destDoc = new Document { VbaProject = doc.VbaProject.Clone() };

	destDoc.Save(ArtifactsDir + "WorkingWithVba.CloneVbaProject.docm");
            
```


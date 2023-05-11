---
title: Clone Vba Module
linktitle: Clone Vba Module
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-vba-macros/clone-vba-module/
---




```csharp
	Document doc = new Document(MyDir + "VBA project.docm");
	Document destDoc = new Document { VbaProject = new VbaProject() };
	
	VbaModule copyModule = doc.VbaProject.Modules["Module1"].Clone();
	destDoc.VbaProject.Modules.Add(copyModule);

	destDoc.Save(ArtifactsDir + "WorkingWithVba.CloneVbaModule.docm");
            
```


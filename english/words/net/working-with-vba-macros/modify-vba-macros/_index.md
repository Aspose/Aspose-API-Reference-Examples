---
title: Modify Vba Macros
linktitle: Modify Vba Macros
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-vba-macros/modify-vba-macros/
---




```csharp
	Document doc = new Document(MyDir + "VBA project.docm");

	VbaProject project = doc.VbaProject;

	const string newSourceCode = "Test change source code";
	project.Modules[0].SourceCode = newSourceCode;
	
	
	doc.Save(ArtifactsDir + "WorkingWithVba.ModifyVbaMacros.docm");
            
```


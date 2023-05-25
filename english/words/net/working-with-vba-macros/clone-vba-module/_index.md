---
title: Clone Vba Module
linktitle: Clone Vba Module
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-vba-macros/clone-vba-module/
---
### Sample source code for Clone Vba Module using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

	Document doc = new Document(dataDir + "VBA project.docm");
	Document destDoc = new Document { VbaProject = new VbaProject() };
	VbaModule copyModule = doc.VbaProject.Modules["Module1"].Clone();
	destDoc.VbaProject.Modules.Add(copyModule);
	destDoc.Save(dataDir + "WorkingWithVba.CloneVbaModule.docm");
```
---
title: Create Vba Project
linktitle: Create Vba Project
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-vba-macros/create-vba-project/
---
### Sample source code for Create Vba Project using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

	Document doc = new Document();
	VbaProject project = new VbaProject();
	project.Name = "AsposeProject";
	doc.VbaProject = project;
	// Create a new module and specify a macro source code.
	VbaModule module = new VbaModule();
	module.Name = "AsposeModule";
	module.Type = VbaModuleType.ProceduralModule;
	module.SourceCode = "New source code";
	// Add module to the VBA project.
	doc.VbaProject.Modules.Add(module);
	doc.Save(dataDir + "WorkingWithVba.CreateVbaProject.docm");
```
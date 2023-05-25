---
title: Clone Vba Project
linktitle: Clone Vba Project
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-vba-macros/clone-vba-project/
---
### Sample source code for Clone Vba Project using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

	Document doc = new Document(dataDir + "VBA project.docm");
	Document destDoc = new Document { VbaProject = doc.VbaProject.Clone() };
	destDoc.Save(dataDir + "WorkingWithVba.CloneVbaProject.docm");
```
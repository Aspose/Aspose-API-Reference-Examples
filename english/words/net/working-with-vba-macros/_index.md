---
title: Working with VBA Macros
linktitle: Working with VBA Macros
second_title: Aspose.Words for .NET API Reference
description: Tutorials containg create vba project, read vba macros, modify vba macros, clone vba project, clone vba module, and remove broken ref using Aspose.Words for .NET
type: docs
weight: 1350
url: /words/net/working-with-vba-macros/
---

Then following tutorials containg create vba project, read vba macros, modify vba macros, clone vba project, clone vba module, and remove broken ref using Aspose.Words for .NET.

## Create Vba Project

```csharp
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

	doc.Save(ArtifactsDir + "WorkingWithVba.CreateVbaProject.docm");
            
```

## Read Vba Macros

```csharp
	Document doc = new Document(MyDir + "VBA project.docm");

	if (doc.VbaProject != null)
	{
		foreach (VbaModule module in doc.VbaProject.Modules)
		{
			Console.WriteLine(module.SourceCode);
		}
	}
            
```

## Modify Vba Macros

```csharp
	Document doc = new Document(MyDir + "VBA project.docm");

	VbaProject project = doc.VbaProject;

	const string newSourceCode = "Test change source code";
	project.Modules[0].SourceCode = newSourceCode;
	
	
	doc.Save(ArtifactsDir + "WorkingWithVba.ModifyVbaMacros.docm");
            
```

## Clone Vba Project

```csharp
	Document doc = new Document(MyDir + "VBA project.docm");
	Document destDoc = new Document { VbaProject = doc.VbaProject.Clone() };

	destDoc.Save(ArtifactsDir + "WorkingWithVba.CloneVbaProject.docm");
            
```

## Clone Vba Module

```csharp
	Document doc = new Document(MyDir + "VBA project.docm");
	Document destDoc = new Document { VbaProject = new VbaProject() };
	
	VbaModule copyModule = doc.VbaProject.Modules["Module1"].Clone();
	destDoc.VbaProject.Modules.Add(copyModule);

	destDoc.Save(ArtifactsDir + "WorkingWithVba.CloneVbaModule.docm");
            
```

## Remove Broken Ref

```csharp
	Document doc = new Document(MyDir + "VBA project.docm");

	// Find and remove the reference with some LibId path.
	const string brokenPath = "brokenPath.dll";
	VbaReferenceCollection references = doc.VbaProject.References;
	for (int i = references.Count - 1; i >= 0; i--)
	{
		VbaReference reference = doc.VbaProject.References.ElementAt(i);

		string path = GetLibIdPath(reference);
		if (path == brokenPath)
			references.RemoveAt(i);
	}

	doc.Save(ArtifactsDir + "WorkingWithVba.RemoveBrokenRef.docm");
            
```

## Get Lib Id Path

```csharp
	private string GetLibIdPath(VbaReference reference)
        {
		switch (reference.Type)
			{
				case VbaReferenceType.Registered:
				case VbaReferenceType.Original:
				case VbaReferenceType.Control:
					return GetLibIdReferencePath(reference.LibId);
				case VbaReferenceType.Project:
					return GetLibIdProjectPath(reference.LibId);
				default:
					throw new ArgumentOutOfRangeException();
			}
		}
```

## Get Lib Id Reference Path

```csharp
	private string GetLibIdReferencePath(string libIdReference)
	{
		if (libIdReference != null)
				{
					string[] refParts = libIdReference.Split('#');
					if (refParts.Length > 3)
						return refParts[3];
				}

				return "";
	}
```

## Get Lib Id Project Path

```csharp
	private string GetLibIdProjectPath(string libIdProject)
	{
	return (libIdProject != null) ? libIdProject.Substring(3) : "";
	}
```


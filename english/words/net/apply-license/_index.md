---
title: How To Apply License
linktitle: How To Apply License
second_title: Aspose.Words for .NET API Reference
description: These examples include how to apply license to Aspose.Words for .NET from file, stream, and other ways in C#.
type: docs
weight: 10
url: /words/net/apply-license/
---

These examples include how to apply license to Aspose.Words for .NET from file, stream, and other ways in C#.

```csharp
##Apply License From File

	License license = new License();

	// This line attempts to set a license from several locations relative to the executable and Aspose.Words.dll.
	// You can also use the additional overload to load a license from a stream, this is useful,
	// for instance, when the license is stored as an embedded resource.
	try
	{
		license.SetLicense("Aspose.Words.lic");
		
		Console.WriteLine("License set successfully.");
	}
	catch (Exception e)
	{
		// We do not ship any license with this example,
		// visit the Aspose site to obtain either a temporary or permanent license. 
		Console.WriteLine("\nThere was an error setting the license: " + e.Message);
	}
```	
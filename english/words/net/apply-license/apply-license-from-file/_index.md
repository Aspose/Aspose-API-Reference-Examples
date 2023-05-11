---
title: Apply License From File
linktitle: Apply License From File
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/apply-license/apply-license-from-file/
---




To license Aspose.Words for .NET through your license, follow these steps:

- Initiate the instance of the [License](/words/net/aspose.words/license/) Class.
- Call [License.SetLicense(string)](/words/net/aspose.words/license/setlicense/#setlicense_1) method with path of your license file.
- [License.SetLicense(string)](/words/net/aspose.words/license/setlicense/#setlicense_1) raises an exception if there is a problem with the license.

```csharp
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
		Console.WriteLine("\nThere was an error setting the license: " + e.Message);
	}
```


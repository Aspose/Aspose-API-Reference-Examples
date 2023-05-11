---
title: Apply License From Stream
linktitle: Apply License From Stream
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/apply-license/apply-license-from-stream/
---



To enable Aspose.Words for .NET license from stream, follow these steps:

- Initialize an instance of the [License](/words/net/aspose.words/license/) class.
- Call the [License.SetLicense(stream)](/words/net/aspose.words/license/setlicense/#setlicense) method.
- [License.SetLicense(stream)](/words/net/aspose.words/license/setlicense/#setlicense_1) throws an exception if there is a problem with the license.

```csharp
	License license = new License();

	try
	{
		license.SetLicense(new MemoryStream(File.ReadAllBytes("Aspose.Words.lic")));
		
		Console.WriteLine("License set successfully.");
	}
	catch (Exception e)
	{
		Console.WriteLine("\nThere was an error setting the license: " + e.Message);
	}
```


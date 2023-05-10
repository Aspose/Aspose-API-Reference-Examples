---
title: Apply License
linktitle: Apply License
second_title: Aspose.Words for .NET API Reference
description: Tutorials of different variations of applying licensing to Aspose.Words for .NET including apply license from file, stream and metered license
type: docs
weight: 10
url: /words/net/apply-license/
---
The following tutorials are different variations of applying licensing to Aspose.Words for .NET including apply license from file, stream and metered license.

## Apply License From File

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

## Apply License From Stream
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

## Apply Metered License
To enable metered license of Aspose.Words for .NET, follow these steps:

- Initialize an instance of the [Metered](/words/net/aspose.words/metered/) class.
- Call the [Metered.SetMeteredKey(string, string)](/words/net/aspose.words/metered/setmeteredkey/) method with public and private key.


```csharp
	try
	{
		Metered metered = new Metered();
		metered.SetMeteredKey("*****", "*****");

		Document doc = new Document(MyDir + "Document.docx");

		Console.WriteLine(doc.PageCount);
	}
	catch (Exception e)
	{
		Console.WriteLine("\nThere was an error setting the license: " + e.Message);
	}
```


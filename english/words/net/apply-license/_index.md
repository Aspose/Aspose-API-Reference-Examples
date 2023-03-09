---
title: apply license
linktitle: apply license
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/apply-license/
---

## Apply License From File

```csharp
        {
            //ExStart:ApplyLicenseFromFile
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
            //ExEnd:ApplyLicenseFromFile
        }

```

## Apply License From Stream

```csharp
        {
            //ExStart:ApplyLicenseFromStream
            License license = new License();

            try
            {
                license.SetLicense(new MemoryStream(File.ReadAllBytes("Aspose.Words.lic")));
                
                Console.WriteLine("License set successfully.");
            }
            catch (Exception e)
            {
                // We do not ship any license with this example,
                // visit the Aspose site to obtain either a temporary or permanent license. 
                Console.WriteLine("\nThere was an error setting the license: " + e.Message);
            }
            //ExEnd:ApplyLicenseFromStream
        }

```

## Apply Metered License

```csharp
        {
            //ExStart:ApplyMeteredLicense
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
            //ExEnd:ApplyMeteredLicense
        }

```


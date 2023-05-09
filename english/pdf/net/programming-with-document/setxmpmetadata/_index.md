---
title: Set XMPMetadata
linktitle: Set XMPMetadata
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 330
url: /pdf/net/programming-with-document/setxmpmetadata/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Open document
            Document pdfDocument = new Document(dataDir + "SetXMPMetadata.pdf");

            // Set properties
            pdfDocument.Metadata["xmp:CreateDate"] = DateTime.Now;
            pdfDocument.Metadata["xmp:Nickname"] = "Nickname";
            pdfDocument.Metadata["xmp:CustomProperty"] = "Custom Value";

            dataDir = dataDir + "SetXMPMetadata_out.pdf";
            // Save document
            pdfDocument.Save(dataDir);
            
            Console.WriteLine("\nXMP metadata in a pdf file setup successfully.\nFile saved at " + dataDir);
        
```


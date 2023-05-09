---
title: Get XMPMetadata
linktitle: Get XMPMetadata
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 200
url: /pdf/net/programming-with-document/getxmpmetadata/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Open document
            Document pdfDocument = new Document(dataDir + "GetXMPMetadata.pdf");

            // Get properties
            Console.WriteLine(pdfDocument.Metadata["xmp:CreateDate"]);
            Console.WriteLine(pdfDocument.Metadata["xmp:Nickname"]);
            Console.WriteLine(pdfDocument.Metadata["xmp:CustomProperty"]);
            
        
```


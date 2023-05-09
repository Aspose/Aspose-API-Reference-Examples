---
title: Set File Info
linktitle: Set File Info
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 310
url: /pdf/net/programming-with-document/setfileinfo/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Open document
            Document pdfDocument = new Document(dataDir + "SetFileInfo.pdf");

            // Specify document information
            DocumentInfo docInfo = new DocumentInfo(pdfDocument);

            docInfo.Author = "Aspose";
            docInfo.CreationDate = DateTime.Now;
            docInfo.Keywords = "Aspose.Pdf, DOM, API";
            docInfo.ModDate = DateTime.Now;
            docInfo.Subject = "PDF Information";
            docInfo.Title = "Setting PDF Document Information";

            dataDir = dataDir + "SetFileInfo_out.pdf";
            // Save output document
            pdfDocument.Save(dataDir);
            
            Console.WriteLine("\nFile informations setup successfully.\nFile saved at " + dataDir);
            
        
```


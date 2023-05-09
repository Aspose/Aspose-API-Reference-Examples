---
title: Get File Info
linktitle: Get File Info
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 180
url: /pdf/net/programming-with-document/getfileinfo/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Open document
            Document pdfDocument = new Document(dataDir + "GetFileInfo.pdf");
            // Get document information
            DocumentInfo docInfo = pdfDocument.Info;
            // Show document information
            Console.WriteLine("Author: {0}", docInfo.Author);
            Console.WriteLine("Creation Date: {0}", docInfo.CreationDate);
            Console.WriteLine("Keywords: {0}", docInfo.Keywords);
            Console.WriteLine("Modify Date: {0}", docInfo.ModDate);
            Console.WriteLine("Subject: {0}", docInfo.Subject);
            Console.WriteLine("Title: {0}", docInfo.Title);
            
        
```


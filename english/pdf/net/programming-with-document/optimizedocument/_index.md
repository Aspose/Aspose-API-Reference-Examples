---
title: Optimize Document
linktitle: Optimize Document
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 240
url: /pdf/net/programming-with-document/optimizedocument/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Open document
            Document pdfDocument = new Document(dataDir + "OptimizeDocument.pdf");

            // Optimize for web
            pdfDocument.Optimize();

            dataDir = dataDir + "OptimizeDocument_out.pdf";

            // Save output document
            pdfDocument.Save(dataDir);
            
            
        
```


---
title: Determine Progress
linktitle: Determine Progress
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 110
url: /pdf/net/programming-with-document/determineprogress/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Open document
            Document pdfDocument = new Document(dataDir + "AddTOC.pdf");
            DocSaveOptions saveOptions = new DocSaveOptions();
            saveOptions.CustomProgressHandler = new UnifiedSaveOptions.ConversionProgressEventHandler(ShowProgressOnConsole);

            dataDir = dataDir + "DetermineProgress_out.pdf";
            pdfDocument.Save(dataDir, saveOptions);
            Console.ReadLine();
            
        
```


---
title: Optimize File Size
linktitle: Optimize File Size
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 250
url: /pdf/net/programming-with-document/optimizefilesize/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Open document
            Document pdfDocument = new Document(dataDir + "OptimizeDocument.pdf");

            OptimizationOptions optimizationOptions = new OptimizationOptions();
            optimizationOptions.LinkDuplcateStreams = true;
            optimizationOptions.RemoveUnusedObjects = true;
            optimizationOptions.RemoveUnusedStreams = true;
            optimizationOptions.ImageCompressionOptions.CompressImages = true;
            optimizationOptions.ImageCompressionOptions.ImageQuality = 10;
            // Optimzie the file size by removing unused objects
            pdfDocument.OptimizeResources(optimizationOptions);
            dataDir = dataDir + "OptimizeFileSize_out.pdf";
            // Save output document
            pdfDocument.Save(dataDir);
            
            
        
```


---
title: Remove Unused Streams
linktitle: Remove Unused Streams
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 270
url: /pdf/net/programming-with-document/removeunusedstreams/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Open document
            Document pdfDocument = new Document(dataDir + "OptimizeDocument.pdf");
            // Set RemoveUsedStreams option 
            var optimizeOptions = new Pdf.Optimization.OptimizationOptions
            {
                RemoveUnusedStreams = true
            };
            // Optimize PDF document using OptimizationOptions
            pdfDocument.OptimizeResources(optimizeOptions);
            dataDir = dataDir + "OptimizeDocument_out.pdf";
            // Save updated document
            pdfDocument.Save(dataDir);
            
            
        
```


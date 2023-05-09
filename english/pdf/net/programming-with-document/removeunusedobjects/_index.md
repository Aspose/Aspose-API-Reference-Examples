---
title: Remove Unused Objects
linktitle: Remove Unused Objects
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 260
url: /pdf/net/programming-with-document/removeunusedobjects/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Open document
            Document pdfDocument = new Document(dataDir + "OptimizeDocument.pdf");
            // Set RemoveUsedObject option 
            var optimizeOptions = new Pdf.Optimization.OptimizationOptions
            {
                RemoveUnusedObjects = true
            };
            // Optimize PDF document using OptimizationOptions
            pdfDocument.OptimizeResources(optimizeOptions);
            dataDir = dataDir + "OptimizeDocument_out.pdf";
            // Save updated document
            pdfDocument.Save(dataDir);
            
        
```


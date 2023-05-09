---
title: Link Duplicate Streams
linktitle: Link Duplicate Streams
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 230
url: /pdf/net/programming-with-document/linkduplicatestreams/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Open document
            Document pdfDocument = new Document(dataDir + "OptimizeDocument.pdf");
            // Set LinkDuplcateStreams option 
            var optimizeOptions = new Pdf.Optimization.OptimizationOptions
            {
                LinkDuplcateStreams = true
            };
            // Optimize PDF document using OptimizationOptions
            pdfDocument.OptimizeResources(optimizeOptions);
            dataDir = dataDir + "OptimizeDocument_out.pdf";
            // Save updated document
            pdfDocument.Save(dataDir);
            
            
        
```


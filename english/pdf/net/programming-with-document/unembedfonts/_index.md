---
title: Unembed Fonts
linktitle: Unembed Fonts
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 370
url: /pdf/net/programming-with-document/unembedfonts/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Open document
            Document pdfDocument = new Document(dataDir + "OptimizeDocument.pdf");
            // Set UnembedFonts  option 
            var optimizeOptions = new Pdf.Optimization.OptimizationOptions
            {
                UnembedFonts = true
            };
            Console.WriteLine("Start");
            // Optimize PDF document using OptimizationOptions
            pdfDocument.OptimizeResources(optimizeOptions);
            // Save updated document
            pdfDocument.Save(dataDir + "OptimizeDocument_out.pdf");
            Console.WriteLine("Finished");
            var fi1 = new System.IO.FileInfo(dataDir + "OptimizeDocument.pdf");
            var fi2 = new System.IO.FileInfo(dataDir + "OptimizeDocument_out.pdf");
            Console.WriteLine("Original file size: {0}. Reduced file size: {1}", fi1.Length, fi2.Length);
            
        
```


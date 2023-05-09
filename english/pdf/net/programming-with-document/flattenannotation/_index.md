---
title: Flatten Annotation
linktitle: Flatten Annotation
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 150
url: /pdf/net/programming-with-document/flattenannotation/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Open document
            Document pdfDocument = new Document(dataDir + "OptimizeDocument.pdf");
            // Flatten annotations
            foreach (var page in pdfDocument.Pages)
            {
                foreach (var annotation in page.Annotations)
                {
                    annotation.Flatten();
                }

            }
            // Save updated document
            pdfDocument.Save(dataDir + "OptimizeDocument_out.pdf");
            
            Console.WriteLine("\nFlattened annotation successfully.\nFile saved at " + dataDir);
        
```


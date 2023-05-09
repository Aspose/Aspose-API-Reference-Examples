---
title: Shrink Documents
linktitle: Shrink Documents
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 350
url: /pdf/net/programming-with-document/shrinkdocuments/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Open document
            Document pdfDocument = new Document(dataDir + "ShrinkDocument.pdf");
            // Optimize PDF document. Note, though, that this method cannot guarantee document shrinking
            pdfDocument.OptimizeResources();
            dataDir = dataDir + "ShrinkDocument_out.pdf";
            // Save updated document
            pdfDocument.Save(dataDir);
            
            
        
```


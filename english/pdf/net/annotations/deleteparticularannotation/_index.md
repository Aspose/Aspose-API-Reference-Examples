---
title: Delete Particular Annotation
linktitle: Delete Particular Annotation
second_title: Aspose.PDF for .NET API Reference
description: The example shows how to delete particular annotation with Aspose.PDF for .NET
type: docs
weight: 50
url: /pdf/net/annotations/deleteparticularannotation/
---
The example shows how to delete particular annotation with Aspose.PDF for .NET


```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Open document
            Document pdfDocument = new Document(dataDir + "DeleteParticularAnnotation.pdf");

            // Delete particular annotation
            pdfDocument.Pages[1].Annotations.Delete(1);

            dataDir = dataDir + "DeleteParticularAnnotation_out.pdf";
            // Save updated document
            pdfDocument.Save(dataDir);
            
            Console.WriteLine("\nParticular annotation deleted successfully.\nFile saved at " + dataDir);
        
```


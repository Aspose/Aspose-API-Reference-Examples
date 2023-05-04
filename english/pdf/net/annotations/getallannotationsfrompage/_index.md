---
title: Get All Annotations From Page
linktitle: Get All Annotations From Page
second_title: Aspose.PDF for .NET API Reference
description: The example shows how to get all annotations from page with Aspose.PDF for .NET
type: docs
weight: 70
url: /pdf/net/annotations/getallannotationsfrompage/
---
The example shows how to get all annotations from page with Aspose.PDF for .NET


```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Open document
            Document pdfDocument = new Document(dataDir + "GetAllAnnotationsFromPage.pdf");

            // Loop through all the annotations
            foreach (MarkupAnnotation annotation in pdfDocument.Pages[1].Annotations)
            {
                // Get annotation properties
                Console.WriteLine("Title : {0} ", annotation.Title);
                Console.WriteLine("Subject : {0} ", annotation.Subject);
                Console.WriteLine("Contents : {0} ", annotation.Contents);                
            }
            
        
```


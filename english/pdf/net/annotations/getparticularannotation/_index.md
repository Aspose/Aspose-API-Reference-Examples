---
title: Get Particular Annotation
linktitle: Get Particular Annotation
second_title: Aspose.PDF for .NET API Reference
description: The example shows how to get particular annotation with Aspose.PDF for .NET
type: docs
weight: 80
url: /pdf/net/annotations/getparticularannotation/
---
The example shows how to get particular annotation with Aspose.PDF for .NET


```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Open document
            Document pdfDocument = new Document(dataDir + "GetParticularAnnotation.pdf");

            // Get particular annotation
            TextAnnotation textAnnotation = (TextAnnotation)pdfDocument.Pages[1].Annotations[1];
            
            // Get annotation properties
            Console.WriteLine("Title : {0} ", textAnnotation.Title);
            Console.WriteLine("Subject : {0} ", textAnnotation.Subject);
            Console.WriteLine("Contents : {0} ", textAnnotation.Contents);
            
        
```


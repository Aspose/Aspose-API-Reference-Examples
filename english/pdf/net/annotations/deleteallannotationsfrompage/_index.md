---
title: Delete All Annotations From Page
linktitle: Delete All Annotations From Page
second_title: Aspose.PDF for .NET API Reference
description: The example shows how to delete all annotations from page with Aspose.PDF for .NET
type: docs
weight: 40
url: /pdf/net/annotations/deleteallannotationsfrompage/
---
The example shows how to delete all annotations from page with Aspose.PDF for .NET


```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Open document
            Document pdfDocument = new Document(dataDir + "DeleteAllAnnotationsFromPage.pdf");

            // Delete particular annotation
            pdfDocument.Pages[1].Annotations.Delete();

            dataDir = dataDir + "DeleteAllAnnotationsFromPage_out.pdf";
            // Save updated document
            pdfDocument.Save(dataDir);
                    
```


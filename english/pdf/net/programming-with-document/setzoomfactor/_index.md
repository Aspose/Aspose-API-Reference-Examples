---
title: Set Zoom Factor
linktitle: Set Zoom Factor
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 340
url: /pdf/net/programming-with-document/setzoomfactor/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Instantiate new Document object
            Document doc = new Document(dataDir + "SetZoomFactor.pdf");

            GoToAction action = new GoToAction(new XYZExplicitDestination(1, 0, 0, .5));
            doc.OpenAction = action;
            dataDir = dataDir + "Zoomed_pdf_out.pdf";
            // Save the document
            doc.Save(dataDir);
            
            
        
```


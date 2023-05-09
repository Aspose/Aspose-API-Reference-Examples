---
title: Get Zoom Factor
linktitle: Get Zoom Factor
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 210
url: /pdf/net/programming-with-document/getzoomfactor/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Instantiate new Document object
            Document doc = new Document(dataDir + "Zoomed_pdf.pdf");

            // Create GoToAction object
            GoToAction action = doc.OpenAction as GoToAction;
            
            // Get the Zoom factor of PDF file
            System.Console.WriteLine((action.Destination as XYZExplicitDestination).Zoom); // Document zoom value;
            
        
```


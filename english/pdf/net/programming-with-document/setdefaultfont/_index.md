---
title: Set Default Font
linktitle: Set Default Font
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 280
url: /pdf/net/programming-with-document/setdefaultfont/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            // Load an existing PDF document with missing font
            string documentName = dataDir + "input.pdf";
            string newName = "Arial";
            using (System.IO.FileStream fs = new System.IO.FileStream(documentName, System.IO.FileMode.Open))
            using (Document document = new Document(fs))
            {
                PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
                // Specify Default Font Name
                pdfSaveOptions.DefaultFontName = newName;
                document.Save(dataDir + "output_out.pdf", pdfSaveOptions);
            }
            
        
```


---
title: Create PDFA1With Aspose Pdf
linktitle: Create PDFA1With Aspose Pdf
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 90
url: /pdf/net/programming-with-document/createpdfa1withasposepdf/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            Aspose.Pdf.Document pdf1 = new Aspose.Pdf.Document();
            // Add a page into the pdf document
            pdf1.Pages.Add().Paragraphs.Add(new TextFragment("Hello World!"));
            MemoryStream ms = new MemoryStream();
            // Save the document
            pdf1.Save(ms);
            pdf1.Convert(new MemoryStream(), PdfFormat.PDF_A_1A, ConvertErrorAction.Delete);
            pdf1.Save(dataDir + "CreatePdfA1_out.pdf");
            
        
```


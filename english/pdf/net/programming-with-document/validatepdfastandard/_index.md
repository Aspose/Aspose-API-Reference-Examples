---
title: Validate PDFAStandard
linktitle: Validate PDFAStandard
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 390
url: /pdf/net/programming-with-document/validatepdfastandard/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Open document
            Document pdfDocument = new Document(dataDir + "ValidatePDFAStandard.pdf");

            // Validate PDF for PDF/A-1a
            pdfDocument.Validate(dataDir + "validation-result-A1A.xml", PdfFormat.PDF_A_1A);
            
        
```


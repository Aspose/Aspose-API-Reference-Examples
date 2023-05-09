---
title: Validate PDFUAstandard
linktitle: Validate PDFUAstandard
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 400
url: /pdf/net/programming-with-document/validatepdfuastandard/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Open document
            Document pdfDocument = new Document(dataDir + "ValidatePDFUAStandard.pdf");

            // Validate PDF for PDF/UA
            bool isValidPdfUa = pdfDocument.Validate(dataDir + "validation-result-UA.xml", PdfFormat.PDF_UA_1);
            
        
```


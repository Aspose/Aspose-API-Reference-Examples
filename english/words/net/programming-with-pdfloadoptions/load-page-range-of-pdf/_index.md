---
title: Load Page Range Of Pdf
linktitle: Load Page Range Of Pdf
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfloadoptions/load-page-range-of-pdf/
---




```csharp

            
            PdfLoadOptions loadOptions = new PdfLoadOptions { PageIndex = 0, PageCount = 1 };

            
            Document doc = new Document(MyDir + "Pdf Document.pdf", loadOptions);

            doc.Save(ArtifactsDir + "WorkingWithPdfLoadOptions.LoadPageRangeOfPdf.pdf");
            
            
        
```


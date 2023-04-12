---
title: Programming With Pdfloadoptions
linktitle: Programming With Pdfloadoptions
second_title: Aspose.Words for .NET API Reference
description: Examples contain load encrypted pdf and load page range of pdf
type: docs
weight: 1620
url: /words/net/programming-with-pdfloadoptions/
---
Examples contain load encrypted pdf and load page range of pdf

## Load Encrypted Pdf

```csharp

            
            Document doc = new Document(MyDir + "Pdf Document.pdf");

            PdfSaveOptions saveOptions = new PdfSaveOptions
            {
                EncryptionDetails = new PdfEncryptionDetails("Aspose", null)
            };

            doc.Save(ArtifactsDir + "WorkingWithPdfLoadOptions.LoadEncryptedPdf.pdf", saveOptions);

            PdfLoadOptions loadOptions = new PdfLoadOptions { Password = "Aspose", LoadFormat = LoadFormat.Pdf };

            doc = new Document(ArtifactsDir + "WorkingWithPdfLoadOptions.LoadEncryptedPdf.pdf", loadOptions);
            
        
```

## Load Page Range Of Pdf

```csharp

            
            PdfLoadOptions loadOptions = new PdfLoadOptions { PageIndex = 0, PageCount = 1 };

            
            Document doc = new Document(MyDir + "Pdf Document.pdf", loadOptions);

            doc.Save(ArtifactsDir + "WorkingWithPdfLoadOptions.LoadPageRangeOfPdf.pdf");
            
            
        
```


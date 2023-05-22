---
title: Load Encrypted Pdf
linktitle: Load Encrypted Pdf
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfloadoptions/load-encrypted-pdf/
---




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


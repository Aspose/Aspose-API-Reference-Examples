---
title: Update Last Printed Property
linktitle: Update Last Printed Property
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/update-last-printed-property/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions { UpdateLastPrintedProperty = true };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.UpdateIfLastPrinted.pdf", saveOptions);
            
        
```


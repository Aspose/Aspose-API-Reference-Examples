---
title: Custom Properties Export
linktitle: Custom Properties Export
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/custom-properties-export/
---




```csharp

            
            Document doc = new Document();
            doc.CustomDocumentProperties.Add("Company", "Aspose");

            PdfSaveOptions saveOptions = new PdfSaveOptions { CustomPropertiesExport = PdfCustomPropertiesExport.Standard };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.CustomPropertiesExport.pdf", saveOptions);
            
        
```


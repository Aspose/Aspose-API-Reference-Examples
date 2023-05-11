---
title: Pdf Render Warnings
linktitle: Pdf Render Warnings
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/pdf-render-warnings/
---




```csharp

            Document doc = new Document(MyDir + "WMF with image.docx");

            MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions
            {
                EmulateRasterOperations = false, RenderingMode = MetafileRenderingMode.VectorWithFallback
            };

            PdfSaveOptions saveOptions = new PdfSaveOptions { MetafileRenderingOptions = metafileRenderingOptions };

            // If Aspose.Words cannot correctly render some of the metafile records
            // to vector graphics then Aspose.Words renders this metafile to a bitmap.
            HandleDocumentWarnings callback = new HandleDocumentWarnings();
            doc.WarningCallback = callback;

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.PdfRenderWarnings.pdf", saveOptions);

            // While the file saves successfully, rendering warnings that occurred during saving are collected here.
            foreach (WarningInfo warningInfo in callback.mWarnings)
            {
                Console.WriteLine(warningInfo.Description);
            }
        
```


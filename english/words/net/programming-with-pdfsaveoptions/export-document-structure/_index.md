---
title: Export Document Structure
linktitle: Export Document Structure
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/export-document-structure/
---




```csharp

            
            Document doc = new Document(MyDir + "Paragraphs.docx");

            // The file size will be increased and the structure will be visible in the "Content" navigation pane
            // of Adobe Acrobat Pro, while editing the .pdf.
            PdfSaveOptions saveOptions = new PdfSaveOptions { ExportDocumentStructure = true };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.ExportDocumentStructure.pdf", saveOptions);
            
        
```


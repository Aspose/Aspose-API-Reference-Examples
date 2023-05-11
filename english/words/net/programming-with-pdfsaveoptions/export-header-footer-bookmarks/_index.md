---
title: Export Header Footer Bookmarks
linktitle: Export Header Footer Bookmarks
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/export-header-footer-bookmarks/
---




```csharp

            
            Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions();
            saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;
            saveOptions.HeaderFooterBookmarksExportMode = HeaderFooterBookmarksExportMode.First;

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.ExportHeaderFooterBookmarks.pdf", saveOptions);
            
        
```


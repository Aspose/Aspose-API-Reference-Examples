---
title: Page By Page
linktitle: Page By Page
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/split-document/page-by-page/
---




```csharp

            
            Document doc = new Document(MyDir + "Big document.docx");

            int pageCount = doc.PageCount;

            for (int page = 0; page < pageCount; page++)
            {
                // Save each page as a separate document.
                Document extractedPage = doc.ExtractPages(page, 1);
                extractedPage.Save(ArtifactsDir + $"SplitDocument.PageByPage_{page + 1}.docx");
            }
            

            MergeDocuments();
        
```


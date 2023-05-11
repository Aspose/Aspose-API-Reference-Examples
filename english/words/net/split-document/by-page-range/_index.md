---
title: By Page Range
linktitle: By Page Range
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/split-document/by-page-range/
---




```csharp

            
            Document doc = new Document(MyDir + "Big document.docx");
            
            // Get part of the document.
            Document extractedPages = doc.ExtractPages(3, 6);
            extractedPages.Save(ArtifactsDir + "SplitDocument.ByPageRange.docx");
            
        
```


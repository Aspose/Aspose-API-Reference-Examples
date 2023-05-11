---
title: By Sections Html
linktitle: By Sections Html
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/split-document/by-sections-html/
---




```csharp

            Document doc = new Document(MyDir + "Rendering.docx");
 
            
            HtmlSaveOptions options = new HtmlSaveOptions { DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak };
            
            
            doc.Save(ArtifactsDir + "SplitDocument.BySectionsHtml.html", options);
        
```


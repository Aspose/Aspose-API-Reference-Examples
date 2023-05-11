---
title: By Headings Html
linktitle: By Headings Html
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/split-document/by-headings-html/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            HtmlSaveOptions options = new HtmlSaveOptions
            {
                // Split a document into smaller parts, in this instance split by heading.
                DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph
            };
            

            doc.Save(ArtifactsDir + "SplitDocument.ByHeadingsHtml.html", options);
            
        
```


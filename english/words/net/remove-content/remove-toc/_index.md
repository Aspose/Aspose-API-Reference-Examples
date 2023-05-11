---
title: Remove Toc
linktitle: Remove Toc
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/remove-content/remove-toc/
---




```csharp

            Document doc = new Document(MyDir + "Table of contents.docx");

            // Remove the first table of contents from the document.
            RemoveTableOfContents(doc, 0);

            doc.Save(ArtifactsDir + "RemoveContent.RemoveToc.doc");
        
```


---
title: Docx To Markdown
linktitle: Docx To Markdown
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/basic-conversions/docx-to-markdown/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Some text!");

            doc.Save(ArtifactsDir + "BaseConversions.DocxToMarkdown.md");
            
        
```


---
title: Apply Paragraph Style
linktitle: Apply Paragraph Style
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-formatting/apply-paragraph-style/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Title;
            builder.Write("Hello");
            
            doc.Save(ArtifactsDir + "DocumentFormatting.ApplyParagraphStyle.docx");
            
        
```


---
title: Insert Html
linktitle: Insert Html
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/insert-html/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.InsertHtml(
                "<P align='right'>Paragraph right</P>" +
                "<b>Implicit paragraph left</b>" +
                "<div align='center'>Div center</div>" +
                "<h1 align='left'>Heading 1 left.</h1>");

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.InsertHtml.docx");
            
        
```


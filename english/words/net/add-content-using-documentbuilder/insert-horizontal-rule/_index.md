---
title: Insert Horizontal Rule
linktitle: Insert Horizontal Rule
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/insert-horizontal-rule/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Insert a horizontal rule shape into the document.");
            builder.InsertHorizontalRule();

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.InsertHorizontalRule.docx");
            
        
```


---
title: Insert Break
linktitle: Insert Break
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/insert-break/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("This is page 1.");
            builder.InsertBreak(BreakType.PageBreak);

            builder.Writeln("This is page 2.");
            builder.InsertBreak(BreakType.PageBreak);

            builder.Writeln("This is page 3.");

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.InsertBreak.docx");
            
        
```


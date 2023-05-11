---
title: Create New Document
linktitle: Create New Document
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/create-new-document/
---




```csharp

            
            Document doc = new Document();

            // Use a document builder to add content to the document.
            DocumentBuilder builder = new DocumentBuilder(doc);
            builder.Writeln("Hello World!");

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.CreateNewDocument.docx");
            
        
```


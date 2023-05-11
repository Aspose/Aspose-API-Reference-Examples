---
title: Move To Document Start End
linktitle: Move To Document Start End
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/move-to-document-start-end/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Move the cursor position to the beginning of your document.
            builder.MoveToDocumentStart();
            Console.WriteLine("\nThis is the beginning of the document.");

            // Move the cursor position to the end of your document.
            builder.MoveToDocumentEnd();
            Console.WriteLine("\nThis is the end of the document.");
            
        
```


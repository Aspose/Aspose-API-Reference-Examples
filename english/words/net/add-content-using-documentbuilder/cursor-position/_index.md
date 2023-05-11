---
title: Cursor Position
linktitle: Cursor Position
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/cursor-position/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Node curNode = builder.CurrentNode;
            Paragraph curParagraph = builder.CurrentParagraph;
            

            Console.WriteLine("\nCursor move to paragraph: " + curParagraph.GetText());
        
```


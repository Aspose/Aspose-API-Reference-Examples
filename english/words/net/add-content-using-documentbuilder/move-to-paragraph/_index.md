---
title: Move To Paragraph
linktitle: Move To Paragraph
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/move-to-paragraph/
---




```csharp

            
            Document doc = new Document(MyDir + "Paragraphs.docx");
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.MoveToParagraph(2, 0);
            builder.Writeln("This is the 3rd paragraph.");
            
        
```


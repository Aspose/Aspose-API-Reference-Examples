---
title: Programming With Ranges
linktitle: Programming With Ranges
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain ranges delete text and ranges get text
type: docs
weight: 1390
url: /words/net/programming-with-ranges/
---
Tutorials contain ranges delete text and ranges get text

## Ranges Delete Text

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");
            doc.Sections[0].Range.Delete();
            
        
```

## Ranges Get Text

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");
            string text = doc.Range.Text;
            
        
```


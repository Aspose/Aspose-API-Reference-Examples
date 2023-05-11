---
title: Get Paragraph Style Separator
linktitle: Get Paragraph Style Separator
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-formatting/get-paragraph-style-separator/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            foreach (Paragraph paragraph in doc.GetChildNodes(NodeType.Paragraph, true))
            {
                if (paragraph.BreakIsStyleSeparator)
                {
                    Console.WriteLine("Separator Found!");
                }
            }
            
        
```


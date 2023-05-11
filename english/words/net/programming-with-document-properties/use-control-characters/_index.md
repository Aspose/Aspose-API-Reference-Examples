---
title: Use Control Characters
linktitle: Use Control Characters
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-properties/use-control-characters/
---




```csharp

            
            const string text = "test\r";
            // Replace "\r" control character with "\r\n".
            string replace = text.Replace(ControlChar.Cr, ControlChar.CrLf);
            
        
```


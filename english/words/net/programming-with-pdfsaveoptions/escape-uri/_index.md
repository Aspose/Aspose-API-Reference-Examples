---
title: Escape Uri
linktitle: Escape Uri
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-pdfsaveoptions/escape-uri/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.InsertHyperlink("Testlink", 
                "https://www.google.com/search?q=%2Fthe%20test", false);
            builder.Writeln();
            builder.InsertHyperlink("https://www.google.com/search?q=%2Fthe%20test", 
                "https://www.google.com/search?q=%2Fthe%20test", false);

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.EscapeUri.pdf");
            
        
```


---
title: Convert Between Measurement Units
linktitle: Convert Between Measurement Units
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-properties/convert-between-measurement-units/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            PageSetup pageSetup = builder.PageSetup;
            pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
            pageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
            pageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
            pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
            pageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
            pageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);
            
        
```


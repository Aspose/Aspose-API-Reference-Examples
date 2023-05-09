---
title: Set Properties For Print Dialog
linktitle: Set Properties For Print Dialog
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 320
url: /pdf/net/programming-with-document/setpropertiesforprintdialog/
---



```csharp

            
            var dataDir = "YOUR DOCUMENT DIRECTORY";

            using (Document doc = new Document())
            {
                doc.Pages.Add();
                doc.Duplex = PrintDuplex.DuplexFlipLongEdge;
                doc.Save(dataDir + "35297_out.pdf", SaveFormat.Pdf);
            }
            
        
```


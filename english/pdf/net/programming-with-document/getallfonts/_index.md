---
title: Get All Fonts
linktitle: Get All Fonts
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 160
url: /pdf/net/programming-with-document/getallfonts/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            Document doc = new Document(dataDir + "input.pdf");
            Aspose.Pdf.Text.Font[] fonts = doc.FontUtilities.GetAllFonts();
            foreach (Aspose.Pdf.Text.Font font in fonts)
            {
                Console.WriteLine(font.FontName);
            }
            
        
```


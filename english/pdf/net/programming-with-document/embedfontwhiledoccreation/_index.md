---
title: Embed Font While Doc Creation
linktitle: Embed Font While Doc Creation
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 140
url: /pdf/net/programming-with-document/embedfontwhiledoccreation/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Instantiate Pdf object by calling its empty constructor
            Aspose.Pdf.Document doc = new Aspose.Pdf.Document();

            // Create a section in the Pdf object
            Aspose.Pdf.Page page = doc.Pages.Add();

            Aspose.Pdf.Text.TextFragment fragment = new Aspose.Pdf.Text.TextFragment("");

            Aspose.Pdf.Text.TextSegment segment = new Aspose.Pdf.Text.TextSegment(" This is a sample text using Custom font.");
            Aspose.Pdf.Text.TextState ts = new Aspose.Pdf.Text.TextState();
            ts.Font = FontRepository.FindFont("Arial");
            ts.Font.IsEmbedded = true;
            segment.TextState = ts;
            fragment.Segments.Add(segment);
            page.Paragraphs.Add(fragment);

            dataDir = dataDir + "EmbedFontWhileDocCreation_out.pdf";
            // Save PDF Document
            doc.Save(dataDir);
            
            
        
```


---
title: Set Free Text Annotation Formatting
linktitle: Set Free Text Annotation Formatting
second_title: Aspose.PDF for .NET API Reference
description: The example shows how to set free text annotation formatting with Aspose.PDF for .NET
type: docs
weight: 140
url: /pdf/net/annotations/setfreetextannotationformatting/
---
The example shows how to set free text annotation formatting with Aspose.PDF for .NET


```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            
            // Open document
            Document pdfDocument = new Document(dataDir + "SetFreeTextAnnotationFormatting.pdf");

            // Instantiate DefaultAppearance object
            DefaultAppearance default_appearance = new DefaultAppearance("Arial", 28, System.Drawing.Color.Red);
            // Create annotation
            FreeTextAnnotation freetext = new FreeTextAnnotation(pdfDocument.Pages[1], new Aspose.Pdf.Rectangle(200, 400, 400, 600), default_appearance);
            // Specify the contents of annotation
            freetext.Contents = "Free Text";
            // Add anootation to annotations collection of page
            pdfDocument.Pages[1].Annotations.Add(freetext);
            dataDir = dataDir + "SetFreeTextAnnotationFormatting_out.pdf";
            // Save the updated document
            pdfDocument.Save(dataDir);            
        
```


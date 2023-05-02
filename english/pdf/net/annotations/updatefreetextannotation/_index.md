---
title: Update Free Text Annotation
linktitle: Update Free Text Annotation
second_title: Aspose.PDF for .NET API Reference
description: The example shows how to update free text annotation with Aspose.PDF for .NET
type: docs
weight: 160
url: /pdf/net/annotations/updatefreetextannotation/
---
The example shows how to update free text annotation with Aspose.PDF for .NET


```csharp

            try
            {
                
                // The path to the documents directory.
                string dataDir = RunExamples.GetDataDir_AsposePdf_Annotations();

                // Open document
                Document doc1 = new Document(dataDir + "input.pdf");

                // Set font size and color of the annotation:
                (doc1.Pages[1].Annotations[0] as FreeTextAnnotation).TextStyle.FontSize = 18;
                (doc1.Pages[1].Annotations[0] as FreeTextAnnotation).TextStyle.Color = System.Drawing.Color.Green;
                
            }
            catch (Exception ex)
            {
                Console.WriteLine(ex.Message);
            }

        
```


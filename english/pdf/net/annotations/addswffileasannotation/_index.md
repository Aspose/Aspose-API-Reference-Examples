---
title: Add Swf File As Annotation
linktitle: Add Swf File As Annotation
second_title: Aspose.PDF for .NET API Reference
description: The example shows how to add swf file as annotation with Aspose.PDF for .NET
type: docs
weight: 30
url: /pdf/net/annotations/addswffileasannotation/
---
The example shows how to add swf file as annotation with Aspose.PDF for .NET


```csharp

            
            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir_AsposePdf_Annotations();

            // Open the PDF document
            Document doc = new Document(dataDir + "AddSwfFileAsAnnotation.pdf");
            
            // Get reference of the page to which you need to add the annotation
            Page page = doc.Pages[1];
            
            // Create ScreenAnnotation object with .swf multimedia file as an argument
            ScreenAnnotation annotation = new ScreenAnnotation(page, new Aspose.Pdf.Rectangle(0, 400, 600, 700), dataDir + "input.swf");
           
            // Add the annotation to annotations collection of page
            page.Annotations.Add(annotation);

            dataDir = dataDir + "AddSwfFileAsAnnotation_out.pdf";
            // Save the update PDF document with annotation
            doc.Save(dataDir);
            
            Console.WriteLine("\nSWF file annotation added to pdf document.\nFile saved at " + dataDir);

        
```


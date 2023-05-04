---
title: Extract Highlighted Text
linktitle: Extract Highlighted Text
second_title: Aspose.PDF for .NET API Reference
description: The example shows how to extract highlighted text with Aspose.PDF for .NET
type: docs
weight: 60
url: /pdf/net/annotations/extracthighlightedtext/
---
The example shows how to extract highlighted text with Aspose.PDF for .NET


```csharp

            
            // The path to the documents directory.
            string dataDir ="YOUR DOCUMENT DIRECTORY";
            Document doc = new Document(dataDir + "ExtractHighlightedText.pdf");
            // Loop through all the annotations
            foreach (Annotation annotation in doc.Pages[1].Annotations)
            {
                // Filter TextMarkupAnnotation
                if (annotation is TextMarkupAnnotation)
                {
                    TextMarkupAnnotation highlightedAnnotation = annotation as TextMarkupAnnotation;
                    // Retrieve highlighted text fragments
                    TextFragmentCollection collection = highlightedAnnotation.GetMarkedTextFragments();
                    foreach (TextFragment tf in collection)
                    {
                        // Display highlighted text
                        Console.WriteLine(tf.Text);
                    }
                }
            }
            
        
```


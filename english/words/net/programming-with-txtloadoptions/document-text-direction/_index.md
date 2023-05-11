---
title: Document Text Direction
linktitle: Document Text Direction
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-txtloadoptions/document-text-direction/
---




```csharp

            
            TxtLoadOptions loadOptions = new TxtLoadOptions { DocumentDirection = DocumentDirection.Auto };

            Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

            Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
            Console.WriteLine(paragraph.ParagraphFormat.Bidi);

            doc.Save(ArtifactsDir + "WorkingWithTxtLoadOptions.DocumentTextDirection.docx");
            
        
```


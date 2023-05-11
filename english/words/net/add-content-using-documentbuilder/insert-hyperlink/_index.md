---
title: Insert Hyperlink
linktitle: Insert Hyperlink
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/insert-hyperlink/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.Write("Please make sure to visit ");
            builder.Font.Color = Color.Blue;
            builder.Font.Underline = Underline.Single;
            
            builder.InsertHyperlink("Aspose Website", "http://www.aspose.com", false);
            
            builder.Font.ClearFormatting();
            builder.Write(" for more information.");

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.InsertHyperlink.docx");
            
        
```


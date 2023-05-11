---
title: Use Destination Styles
linktitle: Use Destination Styles
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/use-destination-styles/
---




```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Append the source document using the styles of the destination document.
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles);

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.UseDestinationStyles.docx");
            
        
```


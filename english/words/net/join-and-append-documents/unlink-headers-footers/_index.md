---
title: Unlink Headers Footers
linktitle: Unlink Headers Footers
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/unlink-headers-footers/
---




```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Unlink the headers and footers in the source document to stop this
            // from continuing the destination document's headers and footers.
            srcDoc.FirstSection.HeadersFooters.LinkToPrevious(false);

            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.UnlinkHeadersFooters.docx");
            
        
```


---
title: Remove Source Headers Footers
linktitle: Remove Source Headers Footers
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/remove-source-headers-footers/
---




```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Remove the headers and footers from each of the sections in the source document.
            foreach (Section section in srcDoc.Sections)
            {
                section.ClearHeadersFooters();
            }

            // Even after the headers and footers are cleared from the source document, the "LinkToPrevious" setting 
            // for HeadersFooters can still be set. This will cause the headers and footers to continue from the destination 
            // document. This should set to false to avoid this behavior.
            srcDoc.FirstSection.HeadersFooters.LinkToPrevious(false);

            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.RemoveSourceHeadersFooters.docx");
            
        
```


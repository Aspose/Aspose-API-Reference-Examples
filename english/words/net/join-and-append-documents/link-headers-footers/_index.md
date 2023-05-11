---
title: Link Headers Footers
linktitle: Link Headers Footers
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/link-headers-footers/
---




```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Set the appended document to appear on a new page.
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.NewPage;
            // Link the headers and footers in the source document to the previous section.
            // This will override any headers or footers already found in the source document.
            srcDoc.FirstSection.HeadersFooters.LinkToPrevious(true);

            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.LinkHeadersFooters.docx");
            
        
```


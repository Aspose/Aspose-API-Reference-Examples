---
title: Move To Headers Footers
linktitle: Move To Headers Footers
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/move-to-headers-footers/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Specify that we want headers and footers different for first, even and odd pages.
            builder.PageSetup.DifferentFirstPageHeaderFooter = true;
            builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

            // Create the headers.
            builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
            builder.Write("Header for the first page");
            builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
            builder.Write("Header for even pages");
            builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
            builder.Write("Header for all other pages");

            // Create two pages in the document.
            builder.MoveToSection(0);
            builder.Writeln("Page1");
            builder.InsertBreak(BreakType.PageBreak);
            builder.Writeln("Page2");

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.MoveToHeadersFooters.docx");
            
        
```


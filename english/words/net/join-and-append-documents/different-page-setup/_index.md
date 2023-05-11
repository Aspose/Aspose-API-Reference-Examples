---
title: Different Page Setup
linktitle: Different Page Setup
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/different-page-setup/
---




```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Set the source document to continue straight after the end of the destination document.
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.Continuous;

            // Restart the page numbering on the start of the source document.
            srcDoc.FirstSection.PageSetup.RestartPageNumbering = true;
            srcDoc.FirstSection.PageSetup.PageStartingNumber = 1;

            // To ensure this does not happen when the source document has different page setup settings, make sure the
            // settings are identical between the last section of the destination document.
            // If there are further continuous sections that follow on in the source document,
            // this will need to be repeated for those sections.
            srcDoc.FirstSection.PageSetup.PageWidth = dstDoc.LastSection.PageSetup.PageWidth;
            srcDoc.FirstSection.PageSetup.PageHeight = dstDoc.LastSection.PageSetup.PageHeight;
            srcDoc.FirstSection.PageSetup.Orientation = dstDoc.LastSection.PageSetup.Orientation;

            // Iterate through all sections in the source document.
            foreach (Paragraph para in srcDoc.GetChildNodes(NodeType.Paragraph, true))
            {
                para.ParagraphFormat.KeepWithNext = true;
            }

            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            
            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.DifferentPageSetup.docx");
            
        
```


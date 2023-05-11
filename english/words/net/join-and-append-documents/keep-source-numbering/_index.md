---
title: Keep Source Numbering
linktitle: Keep Source Numbering
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/keep-source-numbering/
---




```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Keep source list formatting when importing numbered paragraphs.
            ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };
            
            NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting,
                importFormatOptions);

            ParagraphCollection srcParas = srcDoc.FirstSection.Body.Paragraphs;
            foreach (Paragraph srcPara in srcParas)
            {
                Node importedNode = importer.ImportNode(srcPara, false);
                dstDoc.FirstSection.Body.AppendChild(importedNode);
            }

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.KeepSourceNumbering.docx");
            
        
```


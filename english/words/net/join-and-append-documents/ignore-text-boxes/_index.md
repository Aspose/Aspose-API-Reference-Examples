---
title: Ignore Text Boxes
linktitle: Ignore Text Boxes
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/ignore-text-boxes/
---




```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Keep the source text boxes formatting when importing.
            ImportFormatOptions importFormatOptions = new ImportFormatOptions { IgnoreTextBoxes = false };
            
            NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting,
                importFormatOptions);

            ParagraphCollection srcParas = srcDoc.FirstSection.Body.Paragraphs;
            foreach (Paragraph srcPara in srcParas)
            {
                Node importedNode = importer.ImportNode(srcPara, true);
                dstDoc.FirstSection.Body.AppendChild(importedNode);
            }

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.IgnoreTextBoxes.docx");
            
        
```


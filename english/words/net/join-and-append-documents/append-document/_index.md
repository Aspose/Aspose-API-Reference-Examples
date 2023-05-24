---
title: Append Document
linktitle: Append Document
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/append-document/
---




```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");
            
            // Loop through all sections in the source document.
            // Section nodes are immediate children of the Document node so we can just enumerate the Document.
            foreach (Section srcSection in srcDoc)
            {
                // Because we are copying a section from one document to another, 
                // it is required to import the Section node into the destination document.
                // This adjusts any document-specific references to styles, lists, etc.
                //
                // Importing a node creates a copy of the original node, but the copy
                // ss ready to be inserted into the destination document.
                Node dstSection = dstDoc.ImportNode(srcSection, true, ImportFormatMode.KeepSourceFormatting);

                // Now the new section node can be appended to the destination document.
                dstDoc.AppendChild(dstSection);
            }

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.AppendDocument.docx");
            
        
```


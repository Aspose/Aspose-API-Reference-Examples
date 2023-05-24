---
title: Append With Import Format Options
linktitle: Append With Import Format Options
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/append-with-import-format-options/
---




```csharp

            
            Document srcDoc = new Document(MyDir + "Document source with list.docx");
            Document dstDoc = new Document(MyDir + "Document destination with list.docx");

            // Specify that if numbering clashes in source and destination documents,
            // then numbering from the source document will be used.
            ImportFormatOptions options = new ImportFormatOptions { KeepSourceNumbering = true };
            
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);
            
        
```


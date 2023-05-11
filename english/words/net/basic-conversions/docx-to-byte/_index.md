---
title: Docx To Byte
linktitle: Docx To Byte
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/basic-conversions/docx-to-byte/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            MemoryStream outStream = new MemoryStream();
            doc.Save(outStream, SaveFormat.Docx);

            byte[] docBytes = outStream.ToArray();
            MemoryStream inStream = new MemoryStream(docBytes);

            Document docFromBytes = new Document(inStream);
            
        
```


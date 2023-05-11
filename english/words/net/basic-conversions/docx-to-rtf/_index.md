---
title: Docx To Rtf
linktitle: Docx To Rtf
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/basic-conversions/docx-to-rtf/
---




```csharp

            
            
            // Read only access is enough for Aspose.Words to load a document.
            Stream stream = File.OpenRead(MyDir + "Document.docx");

            Document doc = new Document(stream);
            // You can close the stream now, it is no longer needed because the document is in memory.
            stream.Close();
            

            // ... do something with the document.

            // Convert the document to a different format and save to stream.
            MemoryStream dstStream = new MemoryStream();
            doc.Save(dstStream, SaveFormat.Rtf);

            // Rewind the stream position back to zero so it is ready for the next reader.
            dstStream.Position = 0;
            
            
            File.WriteAllBytes(ArtifactsDir + "BaseConversions.DocxToRtf.rtf", dstStream.ToArray());
        
```


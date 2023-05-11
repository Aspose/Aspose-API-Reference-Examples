---
title: Detect Document Signatures
linktitle: Detect Document Signatures
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-fileformat/detect-document-signatures/
---




```csharp

            
            FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Digitally signed.docx");

            if (info.HasDigitalSignature)
            {
                Console.WriteLine(
                    $"Document {Path.GetFileName(MyDir + "Digitally signed.docx")} has digital signatures, " +
                    "they will be lost if you open/save this document with Aspose.Words.");
            }
            
        
```


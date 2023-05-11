---
title: Sign Document
linktitle: Sign Document
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-digital-signatures/sign-document/
---




```csharp

            
            CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
            
            DigitalSignatureUtil.Sign(MyDir + "Digitally signed.docx", ArtifactsDir + "Document.Signed.docx",
                certHolder);
            
        
```


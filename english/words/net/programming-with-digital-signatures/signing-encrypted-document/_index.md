---
title: Signing Encrypted Document
linktitle: Signing Encrypted Document
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-digital-signatures/signing-encrypted-document/
---




```csharp

            
            SignOptions signOptions = new SignOptions { DecryptionPassword = "decryptionPassword" };

            CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
            
            DigitalSignatureUtil.Sign(MyDir + "Digitally signed.docx", ArtifactsDir + "Document.EncryptedDocument.docx",
                certHolder, signOptions);
            
        
```


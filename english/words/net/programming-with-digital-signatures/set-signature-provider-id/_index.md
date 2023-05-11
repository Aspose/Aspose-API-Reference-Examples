---
title: Set Signature Provider Id
linktitle: Set Signature Provider Id
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-digital-signatures/set-signature-provider-id/
---




```csharp

            
            Document doc = new Document(MyDir + "Signature line.docx");

            SignatureLine signatureLine =
                ((Shape) doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true)).SignatureLine;

            SignOptions signOptions = new SignOptions
            {
                ProviderId = signatureLine.ProviderId, SignatureLineId = signatureLine.Id
            };

            CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

            DigitalSignatureUtil.Sign(MyDir + "Digitally signed.docx",
                ArtifactsDir + "SignDocuments.SetSignatureProviderId.docx", certHolder, signOptions);
            
        
```


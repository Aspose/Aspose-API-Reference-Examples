---
title: Signing Existing Signature Line
linktitle: Signing Existing Signature Line
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-digital-signatures/signing-existing-signature-line/
---




```csharp

            
            Document doc = new Document(MyDir + "Signature line.docx");
            
            SignatureLine signatureLine =
                ((Shape) doc.FirstSection.Body.GetChild(NodeType.Shape, 0, true)).SignatureLine;

            SignOptions signOptions = new SignOptions
            {
                SignatureLineId = signatureLine.Id,
                SignatureLineImage = File.ReadAllBytes(ImagesDir + "Enhanced Windows MetaFile.emf")
            };

            CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
            
            DigitalSignatureUtil.Sign(MyDir + "Digitally signed.docx",
                ArtifactsDir + "SignDocuments.SigningExistingSignatureLine.docx", certHolder, signOptions);
            
        
```


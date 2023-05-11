---
title: Creating And Signing New Signature Line
linktitle: Creating And Signing New Signature Line
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-digital-signatures/creating-and-signing-new-signature-line/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            SignatureLine signatureLine = builder.InsertSignatureLine(new SignatureLineOptions()).SignatureLine;
            
            doc.Save(ArtifactsDir + "SignDocuments.SignatureLine.docx");

            SignOptions signOptions = new SignOptions
            {
                SignatureLineId = signatureLine.Id,
                SignatureLineImage = File.ReadAllBytes(ImagesDir + "Enhanced Windows MetaFile.emf")
            };

            CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
            
            DigitalSignatureUtil.Sign(ArtifactsDir + "SignDocuments.SignatureLine.docx",
                ArtifactsDir + "SignDocuments.NewSignatureLine.docx", certHolder, signOptions);
            
        
```


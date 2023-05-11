---
title: Create New Signature Line And Set Provider Id
linktitle: Create New Signature Line And Set Provider Id
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-digital-signatures/create-new-signature-line-and-set-provider-id/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            SignatureLineOptions signatureLineOptions = new SignatureLineOptions
            {
                Signer = "vderyushev",
                SignerTitle = "QA",
                Email = "vderyushev@aspose.com",
                ShowDate = true,
                DefaultInstructions = false,
                Instructions = "Please sign here.",
                AllowComments = true
            };

            SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
            signatureLine.ProviderId = Guid.Parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");
            
            doc.Save(ArtifactsDir + "SignDocuments.SignatureLineProviderId.docx");

            SignOptions signOptions = new SignOptions
            {
                SignatureLineId = signatureLine.Id,
                ProviderId = signatureLine.ProviderId,
                Comments = "Document was signed by vderyushev",
                SignTime = DateTime.Now
            };

            CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

            DigitalSignatureUtil.Sign(ArtifactsDir + "SignDocuments.SignatureLineProviderId.docx", 
                ArtifactsDir + "SignDocuments.CreateNewSignatureLineAndSetProviderId.docx", certHolder, signOptions);
            
        
```


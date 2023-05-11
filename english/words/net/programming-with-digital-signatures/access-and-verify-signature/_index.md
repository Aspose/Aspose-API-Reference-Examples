---
title: Access And Verify Signature
linktitle: Access And Verify Signature
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-digital-signatures/access-and-verify-signature/
---




```csharp

            
            Document doc = new Document(MyDir + "Digitally signed.docx");

            foreach (DigitalSignature signature in doc.DigitalSignatures)
            {
                Console.WriteLine("*** Signature Found ***");
                Console.WriteLine("Is valid: " + signature.IsValid);
                // This property is available in MS Word documents only.
                Console.WriteLine("Reason for signing: " + signature.Comments); 
                Console.WriteLine("Time of signing: " + signature.SignTime);
                Console.WriteLine("Subject name: " + signature.CertificateHolder.Certificate.SubjectName.Name);
                Console.WriteLine("Issuer name: " + signature.CertificateHolder.Certificate.IssuerName.Name);
                Console.WriteLine();
            }
            
        
```


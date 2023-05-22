---
title: Remove Document Protection
linktitle: Remove Document Protection
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-protection/remove-document-protection/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Text added to a document.");

            // Documents can have protection removed either with no password, or with the correct password.
            doc.Unprotect();
            doc.Protect(ProtectionType.ReadOnly, "newPassword");
            doc.Unprotect("newPassword");

            doc.Save(ArtifactsDir + "DocumentProtection.RemoveDocumentProtection.docx");
            
        
```


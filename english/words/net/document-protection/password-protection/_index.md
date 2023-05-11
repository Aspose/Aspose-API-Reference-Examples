---
title: Password Protection
linktitle: Password Protection
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-protection/password-protection/
---




```csharp

            
            Document doc = new Document();

            // Apply document protection.
            doc.Protect(ProtectionType.NoProtection, "password");

            doc.Save(ArtifactsDir + "DocumentProtection.PasswordProtection.docx");
            
        
```


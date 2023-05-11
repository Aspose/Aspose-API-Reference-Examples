---
title: Remove Read Only Restriction
linktitle: Remove Read Only Restriction
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-protection/remove-read-only-restriction/
---




```csharp

            
            Document doc = new Document();
            
            // Enter a password that's up to 15 characters long.
            doc.WriteProtection.SetPassword("MyPassword");

            // Remove the read-only option.
            doc.WriteProtection.ReadOnlyRecommended = false;

            // Apply write protection without any protection.
            doc.Protect(ProtectionType.NoProtection);
            doc.Save(ArtifactsDir + "DocumentProtection.RemoveReadOnlyRestriction.docx");
            
        
```


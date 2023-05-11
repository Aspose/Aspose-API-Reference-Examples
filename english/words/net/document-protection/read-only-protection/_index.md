---
title: Read Only Protection
linktitle: Read Only Protection
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-protection/read-only-protection/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Write("Open document as read-only");

            // Enter a password that's up to 15 characters long.
            doc.WriteProtection.SetPassword("MyPassword");

            // Make the document as read-only.
            doc.WriteProtection.ReadOnlyRecommended = true;

            // Apply write protection as read-only.
            doc.Protect(ProtectionType.ReadOnly);
            doc.Save(ArtifactsDir + "DocumentProtection.ReadOnlyProtection.docx");
            
        
```


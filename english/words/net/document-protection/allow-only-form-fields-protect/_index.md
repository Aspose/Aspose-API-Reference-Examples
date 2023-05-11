---
title: Allow Only Form Fields Protect
linktitle: Allow Only Form Fields Protect
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-protection/allow-only-form-fields-protect/
---




```csharp

            
            // Insert two sections with some text.
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            builder.Writeln("Text added to a document.");

            // A document protection only works when document protection is turned and only editing in form fields is allowed.
            doc.Protect(ProtectionType.AllowOnlyFormFields, "password");

            // Save the protected document.
            doc.Save(ArtifactsDir + "DocumentProtection.AllowOnlyFormFieldsProtect.docx");
            
        
```


---
title: Unrestricted Section
linktitle: Unrestricted Section
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-protection/unrestricted-section/
---




```csharp

            
            // Insert two sections with some text.
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Section 1. Unprotected.");
            builder.InsertBreak(BreakType.SectionBreakContinuous);
            builder.Writeln("Section 2. Protected.");

            // Section protection only works when document protection is turned and only editing in form fields is allowed.
            doc.Protect(ProtectionType.AllowOnlyFormFields, "password");

            // By default, all sections are protected, but we can selectively turn protection off.
            doc.Sections[0].ProtectedForForms = false;
            doc.Save(ArtifactsDir + "DocumentProtection.UnrestrictedSection.docx");

            doc = new Document(ArtifactsDir + "DocumentProtection.UnrestrictedSection.docx");
            Assert.False(doc.Sections[0].ProtectedForForms);
            Assert.True(doc.Sections[1].ProtectedForForms);
            
        
```


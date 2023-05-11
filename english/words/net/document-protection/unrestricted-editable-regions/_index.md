---
title: Unrestricted Editable Regions
linktitle: Unrestricted Editable Regions
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-protection/unrestricted-editable-regions/
---




```csharp

            
            // Upload a document and make it as read-only.
            Document doc = new Document(MyDir + "Document.docx");
            DocumentBuilder builder = new DocumentBuilder(doc);

            doc.Protect(ProtectionType.ReadOnly, "MyPassword");

            builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " + "we cannot edit this paragraph without the password.");

            // Start an editable range.
            EditableRangeStart edRangeStart = builder.StartEditableRange();
            // An EditableRange object is created for the EditableRangeStart that we just made.
            EditableRange editableRange = edRangeStart.EditableRange;

            // Put something inside the editable range.
            builder.Writeln("Paragraph inside first editable range");

            // An editable range is well-formed if it has a start and an end.
            EditableRangeEnd edRangeEnd = builder.EndEditableRange();

            builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

            doc.Save(ArtifactsDir + "DocumentProtection.UnrestrictedEditableRegions.docx");
            
        
```


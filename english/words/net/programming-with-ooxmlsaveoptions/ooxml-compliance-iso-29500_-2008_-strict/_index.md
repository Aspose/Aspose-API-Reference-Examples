---
title: Ooxml Compliance Iso 29500_ 2008_ Strict
linktitle: Ooxml Compliance Iso 29500_ 2008_ Strict
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-ooxmlsaveoptions/ooxml-compliance-iso-29500_-2008_-strict/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2016);
            
            OoxmlSaveOptions saveOptions = new OoxmlSaveOptions() { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

            doc.Save(ArtifactsDir + "WorkingWithOoxmlSaveOptions.OoxmlComplianceIso29500_2008_Strict.docx", saveOptions);
            
        
```


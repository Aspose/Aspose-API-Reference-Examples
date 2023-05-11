---
title: Update Last Saved Time Property
linktitle: Update Last Saved Time Property
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-ooxmlsaveoptions/update-last-saved-time-property/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { UpdateLastSavedTimeProperty = true };

            doc.Save(ArtifactsDir + "WorkingWithOoxmlSaveOptions.UpdateLastSavedTimeProperty.docx", saveOptions);
            
        
```


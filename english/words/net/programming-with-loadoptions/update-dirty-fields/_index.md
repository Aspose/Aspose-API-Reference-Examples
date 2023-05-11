---
title: Update Dirty Fields
linktitle: Update Dirty Fields
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-loadoptions/update-dirty-fields/
---




```csharp

            
            LoadOptions loadOptions = new LoadOptions { UpdateDirtyFields = true };

            Document doc = new Document(MyDir + "Dirty field.docx", loadOptions);

            doc.Save(ArtifactsDir + "WorkingWithLoadOptions.UpdateDirtyFields.docx");
            
        
```


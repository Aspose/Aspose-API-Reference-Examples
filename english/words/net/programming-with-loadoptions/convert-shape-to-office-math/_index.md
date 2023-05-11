---
title: Convert Shape To Office Math
linktitle: Convert Shape To Office Math
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-loadoptions/convert-shape-to-office-math/
---




```csharp

            
            LoadOptions loadOptions = new LoadOptions { ConvertShapeToOfficeMath = true };

            Document doc = new Document(MyDir + "Office math.docx", loadOptions);

            doc.Save(ArtifactsDir + "WorkingWithLoadOptions.ConvertShapeToOfficeMath.docx", SaveFormat.Docx);
            
        
```


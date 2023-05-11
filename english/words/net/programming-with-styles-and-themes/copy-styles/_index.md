---
title: Copy Styles
linktitle: Copy Styles
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-styles-and-themes/copy-styles/
---




```csharp

            
            Document doc = new Document();
            Document target = new Document(MyDir + "Rendering.docx");

            target.CopyStylesFromTemplate(doc);

            doc.Save(ArtifactsDir + "WorkingWithStylesAndThemes.CopyStyles.docx");
            
        
```


---
title: View Options
linktitle: View Options
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-options-and-settings/view-options/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");
            
            doc.ViewOptions.ViewType = ViewType.PageLayout;
            doc.ViewOptions.ZoomPercent = 50;

            doc.Save(ArtifactsDir + "WorkingWithDocumentOptionsAndSettings.ViewOptions.docx");
            
        
```


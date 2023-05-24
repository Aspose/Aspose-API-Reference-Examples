---
title: Auto Fit Table To Page Width
linktitle: Auto Fit Table To Page Width
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/auto-fit-table-to-page-width/
---




```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");

            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            // Autofit the first table to the page width.
            table.AutoFit(AutoFitBehavior.AutoFitToWindow);

            doc.Save(ArtifactsDir + "WorkingWithTables.AutoFitTableToWindow.docx");
            
        
```


---
title: Auto Fit Table To Contents
linktitle: Auto Fit Table To Contents
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/auto-fit-table-to-contents/
---




```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");

            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            table.AutoFit(AutoFitBehavior.AutoFitToContents);

            doc.Save(ArtifactsDir + "WorkingWithTables.AutoFitTableToContents.docx");
            
        
```


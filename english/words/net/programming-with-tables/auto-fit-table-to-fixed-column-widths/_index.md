---
title: Auto Fit Table To Fixed Column Widths
linktitle: Auto Fit Table To Fixed Column Widths
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/auto-fit-table-to-fixed-column-widths/
---




```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");

            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            // Disable autofitting on this table.
            table.AutoFit(AutoFitBehavior.FixedColumnWidths);

            doc.Save(ArtifactsDir + "WorkingWithTables.AutoFitTableToFixedColumnWidths.docx");
            
        
```


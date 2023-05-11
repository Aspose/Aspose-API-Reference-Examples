---
title: Allow Cell Spacing
linktitle: Allow Cell Spacing
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-table-styles-and-formatting/allow-cell-spacing/
---




```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");

            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            table.AllowCellSpacing = true;
            table.CellSpacing = 2;
            
            doc.Save(ArtifactsDir + "WorkingWithTableStylesAndFormatting.AllowCellSpacing.docx");
            
        
```


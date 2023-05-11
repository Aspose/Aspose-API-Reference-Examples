---
title: Modify Cell Formatting
linktitle: Modify Cell Formatting
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-table-styles-and-formatting/modify-cell-formatting/
---




```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);

            Cell firstCell = table.FirstRow.FirstCell;
            firstCell.CellFormat.Width = 30;
            firstCell.CellFormat.Orientation = TextOrientation.Downward;
            firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;
            
        
```


---
title: Expand Formatting On Cells And Row From Style
linktitle: Expand Formatting On Cells And Row From Style
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-table-styles-and-formatting/expand-formatting-on-cells-and-row-from-style/
---




```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");

            // Get the first cell of the first table in the document.
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            Cell firstCell = table.FirstRow.FirstCell;

            // First print the color of the cell shading.
            // This should be empty as the current shading is stored in the table style.
            Color cellShadingBefore = firstCell.CellFormat.Shading.BackgroundPatternColor;
            Console.WriteLine("Cell shading before style expansion: " + cellShadingBefore);

            doc.ExpandTableStylesToDirectFormatting();

            // Now print the cell shading after expanding table styles.
            // A blue background pattern color should have been applied from the table style.
            Color cellShadingAfter = firstCell.CellFormat.Shading.BackgroundPatternColor;
            Console.WriteLine("Cell shading after style expansion: " + cellShadingAfter);
            
        
```


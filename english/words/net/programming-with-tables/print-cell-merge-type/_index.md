---
title: Print Cell Merge Type
linktitle: Print Cell Merge Type
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/print-cell-merge-type/
---
### Sample source code for Print Cell Merge Type using Aspose.Words for .NET 
```csharp
	public string PrintCellMergeType(Cell cell)
        {
            bool isHorizontallyMerged = cell.CellFormat.HorizontalMerge != CellMerge.None;
            bool isVerticallyMerged = cell.CellFormat.VerticalMerge != CellMerge.None;
            string cellLocation =
                $"R{cell.ParentRow.ParentTable.IndexOf(cell.ParentRow) + 1}, C{cell.ParentRow.IndexOf(cell) + 1}";
            if (isHorizontallyMerged && isVerticallyMerged)
                return $"The cell at {cellLocation} is both horizontally and vertically merged";
            if (isHorizontallyMerged)
                return $"The cell at {cellLocation} is horizontally merged.";
            if (isVerticallyMerged)
                return $"The cell at {cellLocation} is vertically merged";
            return $"The cell at {cellLocation} is not merged";
        }
```
---
title: Merge Cell Range
linktitle: Merge Cell Range
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/merge-cell-range/
---




```csharp

            
            Document doc = new Document(MyDir + "Table with merged cells.docx");

            Table table = doc.FirstSection.Body.Tables[0];

            // We want to merge the range of cells found inbetween these two cells.
            Cell cellStartRange = table.Rows[0].Cells[0];
            Cell cellEndRange = table.Rows[1].Cells[1];

            // Merge all the cells between the two specified cells into one.
            MergeCells(cellStartRange, cellEndRange);
            
            doc.Save(ArtifactsDir + "WorkingWithTables.MergeCellRange.docx");
            
        
```


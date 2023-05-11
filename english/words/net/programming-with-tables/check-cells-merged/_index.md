---
title: Check Cells Merged
linktitle: Check Cells Merged
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/check-cells-merged/
---




```csharp

            
            Document doc = new Document(MyDir + "Table with merged cells.docx");

            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);

            foreach (Row row in table.Rows)
            {
                foreach (Cell cell in row.Cells)
                {
                    Console.WriteLine(PrintCellMergeType(cell));
                }
            }
            
        
```


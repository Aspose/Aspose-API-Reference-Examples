---
title: Combine Rows
linktitle: Combine Rows
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/combine-rows/
---




```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");

            // The rows from the second table will be appended to the end of the first table.
            Table firstTable = (Table) doc.GetChild(NodeType.Table, 0, true);
            Table secondTable = (Table) doc.GetChild(NodeType.Table, 1, true);

            // Append all rows from the current table to the next tables
            // with different cell count and widths can be joined into one table.
            while (secondTable.HasChildNodes)
                firstTable.Rows.Add(secondTable.FirstRow);

            secondTable.Remove();

            doc.Save(ArtifactsDir + "WorkingWithTables.CombineRows.docx");
            
        
```

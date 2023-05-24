---
title: Finding Index
linktitle: Finding Index
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/finding-index/
---




```csharp

            Document doc = new Document(MyDir + "Tables.docx");

            
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);

            NodeCollection allTables = doc.GetChildNodes(NodeType.Table, true);
            int tableIndex = allTables.IndexOf(table);
            
            Console.WriteLine("\nTable index is " + tableIndex);

            
            int rowIndex = table.IndexOf(table.LastRow);
            
            Console.WriteLine("\nRow index is " + rowIndex);

            Row row = table.LastRow;
            
            int cellIndex = row.IndexOf(row.Cells[4]);
            
            Console.WriteLine("\nCell index is " + cellIndex);
        
```


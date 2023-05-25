---
title: Finding Index
linktitle: Finding Index
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/finding-index/
---
### Sample source code for Finding Index using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Tables.docx");
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
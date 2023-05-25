---
title: Combine Rows
linktitle: Combine Rows
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/combine-rows/
---
### Sample source code for Combine Rows using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Tables.docx");
            // The rows from the second table will be appended to the end of the first table.
            Table firstTable = (Table) doc.GetChild(NodeType.Table, 0, true);
            Table secondTable = (Table) doc.GetChild(NodeType.Table, 1, true);
            // Append all rows from the current table to the next tables
            // with different cell count and widths can be joined into one table.
            while (secondTable.HasChildNodes)
                firstTable.Rows.Add(secondTable.FirstRow);
            secondTable.Remove();
            doc.Save(dataDir + "WorkingWithTables.CombineRows.docx");
```
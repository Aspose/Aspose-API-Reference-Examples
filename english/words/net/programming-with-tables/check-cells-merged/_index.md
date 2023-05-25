---
title: Check Cells Merged
linktitle: Check Cells Merged
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/check-cells-merged/
---
### Sample source code for Check Cells Merged using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Table with merged cells.docx");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            foreach (Row row in table.Rows)
            {
                foreach (Cell cell in row.Cells)
                {
                    Console.WriteLine(PrintCellMergeType(cell));
                }
            }
```
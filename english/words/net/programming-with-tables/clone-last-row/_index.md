---
title: Clone Last Row
linktitle: Clone Last Row
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/clone-last-row/
---
### Sample source code for Clone Last Row using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Tables.docx");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            Row clonedRow = (Row) table.LastRow.Clone(true);
            // Remove all content from the cloned row's cells. This makes the row ready for new content to be inserted into.
            foreach (Cell cell in clonedRow.Cells)
                cell.RemoveAllChildren();
            table.AppendChild(clonedRow);
            doc.Save(dataDir + "WorkingWithTables.CloneLastRow.docx");
```
---
title: Clone Last Row
linktitle: Clone Last Row
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/clone-last-row/
---




```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");

            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);

            Row clonedRow = (Row) table.LastRow.Clone(true);
            // Remove all content from the cloned row's cells. This makes the row ready for new content to be inserted into.
            foreach (Cell cell in clonedRow.Cells)
                cell.RemoveAllChildren();

            table.AppendChild(clonedRow);

            doc.Save(ArtifactsDir + "WorkingWithTables.CloneLastRow.docx");
            
        
```


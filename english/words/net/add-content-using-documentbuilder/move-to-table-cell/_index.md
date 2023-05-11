---
title: Move To Table Cell
linktitle: Move To Table Cell
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/move-to-table-cell/
---




```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Move the builder to row 3, cell 4 of the first table.
            builder.MoveToCell(0, 2, 3, 0);
            builder.Write("\nCell contents added by DocumentBuilder");
            Table table = (Table)doc.GetChild(NodeType.Table, 0, true);

            Assert.AreEqual(table.Rows[2].Cells[3], builder.CurrentNode.ParentNode.ParentNode);
            Assert.AreEqual("Cell contents added by DocumentBuilderCell 3 contents\a", table.Rows[2].Cells[3].GetText().Trim());
            
        
```


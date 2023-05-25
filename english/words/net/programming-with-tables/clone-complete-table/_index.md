---
title: Clone Complete Table
linktitle: Clone Complete Table
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/clone-complete-table/
---
### Sample source code for Clone Complete Table using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Tables.docx");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            // Clone the table and insert it into the document after the original.
            Table tableClone = (Table) table.Clone(true);
            table.ParentNode.InsertAfter(tableClone, table);
            // Insert an empty paragraph between the two tables,
            // or else they will be combined into one upon saving this has to do with document validation.
            table.ParentNode.InsertAfter(new Paragraph(doc), table);
            doc.Save(dataDir + "WorkingWithTables.CloneCompleteTable.docx");
```
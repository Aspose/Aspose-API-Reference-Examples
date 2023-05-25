---
title: Split Table
linktitle: Split Table
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/split-table/
---
### Sample source code for Split Table using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Tables.docx");
            Table firstTable = (Table) doc.GetChild(NodeType.Table, 0, true);
            // We will split the table at the third row (inclusive).
            Row row = firstTable.Rows[2];
            // Create a new container for the split table.
            Table table = (Table) firstTable.Clone(false);
            // Insert the container after the original.
            firstTable.ParentNode.InsertAfter(table, firstTable);
            // Add a buffer paragraph to ensure the tables stay apart.
            firstTable.ParentNode.InsertAfter(new Paragraph(doc), firstTable);
            Row currentRow;
            do
            {
                currentRow = firstTable.LastRow;
                table.PrependChild(currentRow);
            } while (currentRow != row);
            doc.Save(dataDir + "WorkingWithTables.SplitTable.docx");
```
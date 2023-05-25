---
title: Keep Table Together
linktitle: Keep Table Together
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/keep-table-together/
---
### Sample source code for Keep Table Together using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Table spanning two pages.docx");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            // We need to enable KeepWithNext for every paragraph in the table to keep it from breaking across a page,
            // except for the last paragraphs in the last row of the table.
            foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true))
            {
                cell.EnsureMinimum();
                foreach (Paragraph para in cell.Paragraphs)
                    if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
                        para.ParagraphFormat.KeepWithNext = true;
            }
            doc.Save(dataDir + "WorkingWithTables.KeepTableTogether.docx");
```
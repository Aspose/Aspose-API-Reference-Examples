---
title: Row Format Disable Break Across Pages
linktitle: Row Format Disable Break Across Pages
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/row-format-disable-break-across-pages/
---
### Sample source code for Row Format Disable Break Across Pages using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Table spanning two pages.docx");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            // Disable breaking across pages for all rows in the table.
            foreach (Row row in table.Rows)
                row.RowFormat.AllowBreakAcrossPages = false;
            doc.Save(dataDir + "WorkingWithTables.RowFormatDisableBreakAcrossPages.docx");
```
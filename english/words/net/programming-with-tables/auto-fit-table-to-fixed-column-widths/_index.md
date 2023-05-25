---
title: Auto Fit Table To Fixed Column Widths
linktitle: Auto Fit Table To Fixed Column Widths
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/auto-fit-table-to-fixed-column-widths/
---
### Sample source code for Auto Fit Table To Fixed Column Widths using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Tables.docx");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            // Disable autofitting on this table.
            table.AutoFit(AutoFitBehavior.FixedColumnWidths);
            doc.Save(dataDir + "WorkingWithTables.AutoFitTableToFixedColumnWidths.docx");
```
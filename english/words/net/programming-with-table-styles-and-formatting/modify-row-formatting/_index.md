---
title: Modify Row Formatting
linktitle: Modify Row Formatting
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-table-styles-and-formatting/modify-row-formatting/
---
### Sample source code for Modify Row Formatting using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Tables.docx");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            // Retrieve the first row in the table.
            Row firstRow = table.FirstRow;
            firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
            firstRow.RowFormat.HeightRule = HeightRule.Auto;
            firstRow.RowFormat.AllowBreakAcrossPages = true;
```
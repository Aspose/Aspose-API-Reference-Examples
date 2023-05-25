---
title: Allow Cell Spacing
linktitle: Allow Cell Spacing
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-table-styles-and-formatting/allow-cell-spacing/
---
### Sample source code for Allow Cell Spacing using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Tables.docx");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            table.AllowCellSpacing = true;
            table.CellSpacing = 2;
            doc.Save(dataDir + "WorkingWithTableStylesAndFormatting.AllowCellSpacing.docx");
```
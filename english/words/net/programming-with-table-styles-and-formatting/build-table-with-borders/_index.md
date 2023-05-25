---
title: Build Table With Borders
linktitle: Build Table With Borders
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-table-styles-and-formatting/build-table-with-borders/
---
### Sample source code for Build Table With Borders using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Tables.docx");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            // Clear any existing borders from the table.
            table.ClearBorders();
            // Set a green border around and inside the table.
            table.SetBorders(LineStyle.Single, 1.5, Color.Green);
            doc.Save(dataDir + "WorkingWithTableStylesAndFormatting.BuildTableWithBorders.docx");
```
---
title: Auto Fit Table To Page Width
linktitle: Auto Fit Table To Page Width
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/auto-fit-table-to-page-width/
---
### Sample source code for Auto Fit Table To Page Width using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Tables.docx");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            // Autofit the first table to the page width.
            table.AutoFit(AutoFitBehavior.AutoFitToWindow);
            doc.Save(dataDir + "WorkingWithTables.AutoFitTableToWindow.docx");
```
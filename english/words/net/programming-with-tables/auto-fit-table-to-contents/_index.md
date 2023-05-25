---
title: Auto Fit Table To Contents
linktitle: Auto Fit Table To Contents
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/auto-fit-table-to-contents/
---
### Sample source code for Auto Fit Table To Contents using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Tables.docx");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            table.AutoFit(AutoFitBehavior.AutoFitToContents);
            doc.Save(dataDir + "WorkingWithTables.AutoFitTableToContents.docx");
```
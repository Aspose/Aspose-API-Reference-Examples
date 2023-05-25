---
title: Get Distance Between Table Surrounding Text
linktitle: Get Distance Between Table Surrounding Text
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-table-styles-and-formatting/get-distance-between-table-surrounding-text/
---
### Sample source code for Get Distance Between Table Surrounding Text using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Tables.docx");
            Console.WriteLine("\nGet distance between table left, right, bottom, top and the surrounding text.");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            Console.WriteLine(table.DistanceTop);
            Console.WriteLine(table.DistanceBottom);
            Console.WriteLine(table.DistanceRight);
            Console.WriteLine(table.DistanceLeft);
```
---
title: Get Distance Between Table Surrounding Text
linktitle: Get Distance Between Table Surrounding Text
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-table-styles-and-formatting/get-distance-between-table-surrounding-text/
---




```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");

            Console.WriteLine("\nGet distance between table left, right, bottom, top and the surrounding text.");
            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);

            Console.WriteLine(table.DistanceTop);
            Console.WriteLine(table.DistanceBottom);
            Console.WriteLine(table.DistanceRight);
            Console.WriteLine(table.DistanceLeft);
            
        
```


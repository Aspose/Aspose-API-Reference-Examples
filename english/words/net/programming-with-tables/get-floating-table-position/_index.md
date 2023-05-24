---
title: Get Floating Table Position
linktitle: Get Floating Table Position
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/get-floating-table-position/
---




```csharp

            
            Document doc = new Document(MyDir + "Table wrapped by text.docx");
            
            foreach (Table table in doc.FirstSection.Body.Tables)
            {
                // If the table is floating type, then print its positioning properties.
                if (table.TextWrapping == TextWrapping.Around)
                {
                    Console.WriteLine(table.HorizontalAnchor);
                    Console.WriteLine(table.VerticalAnchor);
                    Console.WriteLine(table.AbsoluteHorizontalDistance);
                    Console.WriteLine(table.AbsoluteVerticalDistance);
                    Console.WriteLine(table.AllowOverlap);
                    Console.WriteLine(table.AbsoluteHorizontalDistance);
                    Console.WriteLine(table.RelativeVerticalAlignment);
                    Console.WriteLine("..............................");
                }
            }
            
        
```


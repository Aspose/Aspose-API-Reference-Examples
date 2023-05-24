---
title: Build Table With Borders
linktitle: Build Table With Borders
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-table-styles-and-formatting/build-table-with-borders/
---




```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");

            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            
            // Clear any existing borders from the table.
            table.ClearBorders();
            
            // Set a green border around and inside the table.
            table.SetBorders(LineStyle.Single, 1.5, Color.Green);

            doc.Save(ArtifactsDir + "WorkingWithTableStylesAndFormatting.BuildTableWithBorders.docx");
            
        
```


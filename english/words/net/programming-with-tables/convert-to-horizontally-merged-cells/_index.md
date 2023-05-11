---
title: Convert To Horizontally Merged Cells
linktitle: Convert To Horizontally Merged Cells
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/convert-to-horizontally-merged-cells/
---




```csharp

            
            Document doc = new Document(MyDir + "Table with merged cells.docx");

            Table table = doc.FirstSection.Body.Tables[0];
            // Now merged cells have appropriate merge flags.
            table.ConvertToHorizontallyMergedCells();
            
        
```


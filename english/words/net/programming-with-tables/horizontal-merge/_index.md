---
title: Horizontal Merge
linktitle: Horizontal Merge
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/horizontal-merge/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertCell();
            builder.CellFormat.HorizontalMerge = CellMerge.First;
            builder.Write("Text in merged cells.");

            builder.InsertCell();
            // This cell is merged to the previous and should be empty.
            builder.CellFormat.HorizontalMerge = CellMerge.Previous;
            builder.EndRow();

            builder.InsertCell();
            builder.CellFormat.HorizontalMerge = CellMerge.None;
            builder.Write("Text in one cell.");

            builder.InsertCell();
            builder.Write("Text in another cell.");
            builder.EndRow();
            builder.EndTable();
            
            doc.Save(ArtifactsDir + "WorkingWithTables.HorizontalMerge.docx");
            
        
```

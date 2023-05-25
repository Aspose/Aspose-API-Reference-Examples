---
title: Vertical Merge
linktitle: Vertical Merge
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/vertical-merge/
---
### Sample source code for Vertical Merge using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            builder.InsertCell();
            builder.CellFormat.VerticalMerge = CellMerge.First;
            builder.Write("Text in merged cells.");
            builder.InsertCell();
            builder.CellFormat.VerticalMerge = CellMerge.None;
            builder.Write("Text in one cell");
            builder.EndRow();
            builder.InsertCell();
            // This cell is vertically merged to the cell above and should be empty.
            builder.CellFormat.VerticalMerge = CellMerge.Previous;
            builder.InsertCell();
            builder.CellFormat.VerticalMerge = CellMerge.None;
            builder.Write("Text in another cell");
            builder.EndRow();
            builder.EndTable();
            doc.Save(dataDir + "WorkingWithTables.VerticalMerge.docx");
```
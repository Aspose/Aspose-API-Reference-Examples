---
title: Set Cell Padding
linktitle: Set Cell Padding
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-table-styles-and-formatting/set-cell-padding/
---
### Sample source code for Set Cell Padding using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            builder.StartTable();
            builder.InsertCell();
            // Sets the amount of space (in points) to add to the left/top/right/bottom of the cell's contents.
            builder.CellFormat.SetPaddings(30, 50, 30, 50);
            builder.Writeln("I'm a wonderful formatted cell.");
            builder.EndRow();
            builder.EndTable();
            doc.Save(dataDir + "WorkingWithTableStylesAndFormatting.SetCellPadding.docx");
```
---
title: Build Table
linktitle: Build Table
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/build-table/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Table table = builder.StartTable();
            builder.InsertCell();
            table.AutoFit(AutoFitBehavior.FixedColumnWidths);

            builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
            builder.Write("This is row 1 cell 1");

            builder.InsertCell();
            builder.Write("This is row 1 cell 2");

            builder.EndRow();

            builder.InsertCell();
            
            builder.RowFormat.Height = 100;
            builder.RowFormat.HeightRule = HeightRule.Exactly;
            builder.CellFormat.Orientation = TextOrientation.Upward;
            builder.Writeln("This is row 2 cell 1");

            builder.InsertCell();
            builder.CellFormat.Orientation = TextOrientation.Downward;
            builder.Writeln("This is row 2 cell 2");

            builder.EndRow();
            builder.EndTable();

            doc.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.BuildTable.docx");
            
        
```


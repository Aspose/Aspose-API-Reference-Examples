---
title: Auto Fit To Page Width
linktitle: Auto Fit To Page Width
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/auto-fit-to-page-width/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Insert a table with a width that takes up half the page width.
            Table table = builder.StartTable();

            builder.InsertCell();
            table.PreferredWidth = PreferredWidth.FromPercent(50);
            builder.Writeln("Cell #1");

            builder.InsertCell();
            builder.Writeln("Cell #2");

            builder.InsertCell();
            builder.Writeln("Cell #3");

            doc.Save(ArtifactsDir + "WorkingWithTables.AutoFitToPageWidth.docx");
            
        
```

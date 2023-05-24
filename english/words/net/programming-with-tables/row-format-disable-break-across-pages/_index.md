---
title: Row Format Disable Break Across Pages
linktitle: Row Format Disable Break Across Pages
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/row-format-disable-break-across-pages/
---




```csharp

            
            Document doc = new Document(MyDir + "Table spanning two pages.docx");

            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);

            // Disable breaking across pages for all rows in the table.
            foreach (Row row in table.Rows)
                row.RowFormat.AllowBreakAcrossPages = false;

            doc.Save(ArtifactsDir + "WorkingWithTables.RowFormatDisableBreakAcrossPages.docx");
            
        
```


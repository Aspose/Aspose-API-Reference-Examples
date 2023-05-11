---
title: Set Table Title And Description
linktitle: Set Table Title And Description
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-table-styles-and-formatting/set-table-title-and-description/
---




```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");

            Table table = (Table) doc.GetChild(NodeType.Table, 0, true);
            table.Title = "Test title";
            table.Description = "Test description";

            OoxmlSaveOptions options = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

            doc.CompatibilityOptions.OptimizeFor(Aspose.Words.Settings.MsWordVersion.Word2016);

            doc.Save(ArtifactsDir + "WorkingWithTableStylesAndFormatting.SetTableTitleAndDescription.docx", options);
            
        
```


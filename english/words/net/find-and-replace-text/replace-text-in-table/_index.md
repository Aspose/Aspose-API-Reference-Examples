---
title: Replace Text In Table
linktitle: Replace Text In Table
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/find-and-replace-text/replace-text-in-table/
---




```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");

            Table table = (Table)doc.GetChild(NodeType.Table, 0, true);

            table.Range.Replace("Carrots", "Eggs", new FindReplaceOptions(FindReplaceDirection.Forward));
            table.LastRow.LastCell.Range.Replace("50", "20", new FindReplaceOptions(FindReplaceDirection.Forward));

            doc.Save(ArtifactsDir + "FindAndReplace.ReplaceTextInTable.docx");
            
        
```


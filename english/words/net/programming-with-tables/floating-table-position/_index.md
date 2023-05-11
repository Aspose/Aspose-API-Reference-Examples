---
title: Floating Table Position
linktitle: Floating Table Position
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/floating-table-position/
---




```csharp

            
            Document doc = new Document(MyDir + "Table wrapped by text.docx");

            Table table = doc.FirstSection.Body.Tables[0];
            table.AbsoluteHorizontalDistance = 10;
            table.RelativeVerticalAlignment = VerticalAlignment.Center;

            doc.Save(ArtifactsDir + "WorkingWithTables.FloatingTablePosition.docx");
            
        
```


---
title: Floating Table Position
linktitle: Floating Table Position
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/floating-table-position/
---
### Sample source code for Floating Table Position using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Table wrapped by text.docx");
            Table table = doc.FirstSection.Body.Tables[0];
            table.AbsoluteHorizontalDistance = 10;
            table.RelativeVerticalAlignment = VerticalAlignment.Center;
            doc.Save(dataDir + "WorkingWithTables.FloatingTablePosition.docx");
```
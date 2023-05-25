---
title: Set Relative Horizontal Or Vertical Position
linktitle: Set Relative Horizontal Or Vertical Position
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-tables/set-relative-horizontal-or-vertical-position/
---
### Sample source code for Set Relative Horizontal Or Vertical Position using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Table wrapped by text.docx");
            Table table = doc.FirstSection.Body.Tables[0];
            table.HorizontalAnchor = RelativeHorizontalPosition.Column;
            table.VerticalAnchor = RelativeVerticalPosition.Page;
            doc.Save(dataDir + "WorkingWithTables.SetFloatingTablePosition.docx");
```
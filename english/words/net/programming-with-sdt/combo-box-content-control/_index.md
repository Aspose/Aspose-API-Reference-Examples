---
title: Combo Box Content Control
linktitle: Combo Box Content Control
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/combo-box-content-control/
---
### Sample source code for Combo Box Content Control using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            StructuredDocumentTag sdt = new StructuredDocumentTag(doc, SdtType.ComboBox, MarkupLevel.Block);
            sdt.ListItems.Add(new SdtListItem("Choose an item", "-1"));
            sdt.ListItems.Add(new SdtListItem("Item 1", "1"));
            sdt.ListItems.Add(new SdtListItem("Item 2", "2"));
            doc.FirstSection.Body.AppendChild(sdt);
            doc.Save(dataDir + "WorkingWithSdt.ComboBoxContentControl.docx");
```
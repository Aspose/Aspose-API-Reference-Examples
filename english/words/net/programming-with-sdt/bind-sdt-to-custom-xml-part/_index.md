---
title: Bind SDT to Custom Xml Part
linktitle: Bind SDT to Custom Xml Part
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/bind-sdt-to-custom-xml-part/
---
### Sample source code for Bind Sd Tto Custom Xml Part using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            CustomXmlPart xmlPart =
                doc.CustomXmlParts.Add(Guid.NewGuid().ToString("B"), "<root><text>Hello, World!</text></root>");
            StructuredDocumentTag sdt = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
            doc.FirstSection.Body.AppendChild(sdt);
            sdt.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", "");
            doc.Save(dataDir + "WorkingWithSdt.BindSDTtoCustomXmlPart.doc");
```
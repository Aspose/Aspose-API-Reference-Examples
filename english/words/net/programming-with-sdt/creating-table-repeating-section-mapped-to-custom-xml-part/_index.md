---
title: Creating Table Repeating Section Mapped To Custom Xml Part
linktitle: Creating Table Repeating Section Mapped To Custom Xml Part
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/creating-table-repeating-section-mapped-to-custom-xml-part/
---
### Sample source code for Creating Table Repeating Section Mapped To Custom Xml Part using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            CustomXmlPart xmlPart = doc.CustomXmlParts.Add("Books",
                "<books><book><title>Everyday Italian</title><author>Giada De Laurentiis</author></book>" +
                "<book><title>Harry Potter</title><author>J K. Rowling</author></book>" +
                "<book><title>Learning XML</title><author>Erik T. Ray</author></book></books>");
            Table table = builder.StartTable();
            builder.InsertCell();
            builder.Write("Title");
            builder.InsertCell();
            builder.Write("Author");
            builder.EndRow();
            builder.EndTable();
            StructuredDocumentTag repeatingSectionSdt =
                new StructuredDocumentTag(doc, SdtType.RepeatingSection, MarkupLevel.Row);
            repeatingSectionSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book", "");
            table.AppendChild(repeatingSectionSdt);
            StructuredDocumentTag repeatingSectionItemSdt = 
                new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
            repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);
            Row row = new Row(doc);
            repeatingSectionItemSdt.AppendChild(row);
            StructuredDocumentTag titleSdt =
                new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
            titleSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/title[1]", "");
            row.AppendChild(titleSdt);
            StructuredDocumentTag authorSdt =
                new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
            authorSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/author[1]", "");
            row.AppendChild(authorSdt);
            doc.Save(dataDir + "WorkingWithSdt.CreatingTableRepeatingSectionMappedToCustomXmlPart.docx");
```
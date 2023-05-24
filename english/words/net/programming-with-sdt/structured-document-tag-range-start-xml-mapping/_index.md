---
title: Structured Document Tag Range Start Xml Mapping
linktitle: Structured Document Tag Range Start Xml Mapping
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/structured-document-tag-range-start-xml-mapping/
---




```csharp

            
            Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

            // Construct an XML part that contains data and add it to the document's CustomXmlPart collection.
            string xmlPartId = Guid.NewGuid().ToString("B");
            string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
            CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);
            Console.WriteLine(Encoding.UTF8.GetString(xmlPart.Data));

            // Create a StructuredDocumentTag that will display the contents of our CustomXmlPart in the document.
            StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

            // If we set a mapping for our StructuredDocumentTag,
            // it will only display a part of the CustomXmlPart that the XPath points to.
            // This XPath will point to the contents second "<text>" element of the first "<root>" element of our CustomXmlPart.
            sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

            doc.Save(ArtifactsDir + "WorkingWithSdt.StructuredDocumentTagRangeStartXmlMapping.docx");
            
        
```


---
title: Configuring Link To Content
linktitle: Configuring Link To Content
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-properties/configuring-link-to-content/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.StartBookmark("MyBookmark");
            builder.Writeln("Text inside a bookmark.");
            builder.EndBookmark("MyBookmark");

            // Retrieve a list of all custom document properties from the file.
            CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
            // Add linked to content property.
            DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");
            customProperty = customProperties["Bookmark"];

            bool isLinkedToContent = customProperty.IsLinkToContent;
            
            string linkSource = customProperty.LinkSource;
            
            string customPropertyValue = customProperty.Value.ToString();
            
        
```


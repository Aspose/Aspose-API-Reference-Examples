---
title: Add Custom Document Properties
linktitle: Add Custom Document Properties
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-properties/add-custom-document-properties/
---




```csharp

            
            Document doc = new Document(MyDir + "Properties.docx");

            CustomDocumentProperties customDocumentProperties = doc.CustomDocumentProperties;
            
            if (customDocumentProperties["Authorized"] != null) return;
            
            customDocumentProperties.Add("Authorized", true);
            customDocumentProperties.Add("Authorized By", "John Smith");
            customDocumentProperties.Add("Authorized Date", DateTime.Today);
            customDocumentProperties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
            customDocumentProperties.Add("Authorized Amount", 123.45);
            
        
```


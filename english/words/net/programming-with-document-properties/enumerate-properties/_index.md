---
title: Enumerate Properties
linktitle: Enumerate Properties
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-properties/enumerate-properties/
---




```csharp

            
            Document doc = new Document(MyDir + "Properties.docx");
            
            Console.WriteLine("1. Document name: {0}", doc.OriginalFileName);
            Console.WriteLine("2. Built-in Properties");
            
            foreach (DocumentProperty prop in doc.BuiltInDocumentProperties)
                Console.WriteLine("{0} : {1}", prop.Name, prop.Value);

            Console.WriteLine("3. Custom Properties");
            
            foreach (DocumentProperty prop in doc.CustomDocumentProperties)
                Console.WriteLine("{0} : {1}", prop.Name, prop.Value);
            
        
```


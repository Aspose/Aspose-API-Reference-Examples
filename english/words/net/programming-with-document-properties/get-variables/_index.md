---
title: Get Variables
linktitle: Get Variables
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-properties/get-variables/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");
            
            string variables = "";
            foreach (KeyValuePair<string, string> entry in doc.Variables)
            {
                string name = entry.Key;
                string value = entry.Value;
                if (variables == "")
                {
                    variables = "Name: " + name + "," + "Value: {1}" + value;
                }
                else
                {
                    variables = variables + "Name: " + name + "," + "Value: {1}" + value;
                }
            }
            

            Console.WriteLine("\nDocument have following variables " + variables);
        
```


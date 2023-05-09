---
title: Get Warnings For Font Substitution
linktitle: Get Warnings For Font Substitution
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 190
url: /pdf/net/programming-with-document/getwarningsforfontsubstitution/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "input.pdf");

            doc.FontSubstitution += new Document.FontSubstitutionHandler(OnFontSubstitution);
            
        
```


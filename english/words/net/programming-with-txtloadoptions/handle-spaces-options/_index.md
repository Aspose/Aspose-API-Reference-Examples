---
title: Handle Spaces Options
linktitle: Handle Spaces Options
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-txtloadoptions/handle-spaces-options/
---




```csharp

            
            const string textDoc = "      Line 1 \n" +
                                   "    Line 2   \n" +
                                   " Line 3       ";

            TxtLoadOptions loadOptions = new TxtLoadOptions
            {
                LeadingSpacesOptions = TxtLeadingSpacesOptions.Trim,
                TrailingSpacesOptions = TxtTrailingSpacesOptions.Trim
            };

            Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);

            doc.Save(ArtifactsDir + "WorkingWithTxtLoadOptions.HandleSpacesOptions.docx");
            
        
```


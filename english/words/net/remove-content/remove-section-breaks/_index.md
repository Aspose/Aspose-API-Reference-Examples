---
title: Remove Section Breaks
linktitle: Remove Section Breaks
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/remove-content/remove-section-breaks/
---




```csharp

            // Loop through all sections starting from the section that precedes the last one and moving to the first section.
            for (int i = doc.Sections.Count - 2; i >= 0; i--)
            {
                // Copy the content of the current section to the beginning of the last section.
                doc.LastSection.PrependContent(doc.Sections[i]);
                // Remove the copied section.
                doc.Sections[i].Remove();
            }
        
```


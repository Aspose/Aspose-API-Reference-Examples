---
title: Remove Footers
linktitle: Remove Footers
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/remove-content/remove-footers/
---




```csharp

            
            Document doc = new Document(MyDir + "Header and footer types.docx");

            foreach (Section section in doc)
            {
                // Up to three different footers are possible in a section (for first, even and odd pages)
                // we check and delete all of them.
                HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
                footer?.Remove();

                // Primary footer is the footer used for odd pages.
                footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
                footer?.Remove();

                footer = section.HeadersFooters[HeaderFooterType.FooterEven];
                footer?.Remove();
            }

            doc.Save(ArtifactsDir + "RemoveContent.RemoveFooters.docx");
            
        
```


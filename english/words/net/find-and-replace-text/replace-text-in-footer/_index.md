---
title: Replace Text In Footer
linktitle: Replace Text In Footer
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/find-and-replace-text/replace-text-in-footer/
---




```csharp

            
            Document doc = new Document(MyDir + "Footer.docx");

            HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
            HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

            FindReplaceOptions options = new FindReplaceOptions { MatchCase = false, FindWholeWordsOnly = false };

            footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", "Copyright (C) 2020 by Aspose Pty Ltd.", options);

            doc.Save(ArtifactsDir + "FindAndReplace.ReplaceTextInFooter.docx");
            
        
```


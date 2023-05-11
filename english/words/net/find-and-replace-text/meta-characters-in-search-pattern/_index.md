---
title: Meta Characters In Search Pattern
linktitle: Meta Characters In Search Pattern
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/find-and-replace-text/meta-characters-in-search-pattern/
---




```csharp

            /* meta-characters
            &p - paragraph break
            &b - section break
            &m - page break
            &l - manual line break
            */

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.Writeln("This is Line 1");
            builder.Writeln("This is Line 2");

            doc.Range.Replace("This is Line 1&pThis is Line 2", "This is replaced line");

            builder.MoveToDocumentEnd();
            builder.Write("This is Line 1");
            builder.InsertBreak(BreakType.PageBreak);
            builder.Writeln("This is Line 2");

            doc.Range.Replace("This is Line 1&mThis is Line 2", "Page break is replaced with new text.");

            doc.Save(ArtifactsDir + "FindAndReplace.MetaCharactersInSearchPattern.docx");
            
        
```


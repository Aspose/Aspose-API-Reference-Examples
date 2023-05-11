---
title: Replace Text Containing Meta Characters
linktitle: Replace Text Containing Meta Characters
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/find-and-replace-text/replace-text-containing-meta-characters/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Arial";
            builder.Writeln("First section");
            builder.Writeln("  1st paragraph");
            builder.Writeln("  2nd paragraph");
            builder.Writeln("{insert-section}");
            builder.Writeln("Second section");
            builder.Writeln("  1st paragraph");

            FindReplaceOptions findReplaceOptions = new FindReplaceOptions();
            findReplaceOptions.ApplyParagraphFormat.Alignment = ParagraphAlignment.Center;

            // Double each paragraph break after word "section", add kind of underline and make it centered.
            int count = doc.Range.Replace("section&p", "section&p----------------------&p", findReplaceOptions);

            // Insert section break instead of custom text tag.
            count = doc.Range.Replace("{insert-section}", "&b", findReplaceOptions);

            doc.Save(ArtifactsDir + "FindAndReplace.ReplaceTextContainingMetaCharacters.docx");
            
        
```


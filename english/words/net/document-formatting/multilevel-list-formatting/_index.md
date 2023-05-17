---
title: Multilevel List Formatting
linktitle: Multilevel List Formatting
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/document-formatting/multilevel-list-formatting/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ListFormat.ApplyNumberDefault();
            builder.Writeln("Item 1");
            builder.Writeln("Item 2");

            builder.ListFormat.ListIndent();
            builder.Writeln("Item 2.1");
            builder.Writeln("Item 2.2");
            
            builder.ListFormat.ListIndent();
            builder.Writeln("Item 2.2.1");
            builder.Writeln("Item 2.2.2");

            builder.ListFormat.ListOutdent();
            builder.Writeln("Item 2.3");

            builder.ListFormat.ListOutdent();
            builder.Writeln("Item 3");

            builder.ListFormat.RemoveNumbers();
            
            doc.Save(ArtifactsDir + "DocumentFormatting.MultilevelListFormatting.docx");
            
        
```


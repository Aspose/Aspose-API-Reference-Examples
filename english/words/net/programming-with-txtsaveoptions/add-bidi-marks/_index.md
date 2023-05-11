---
title: Add Bidi Marks
linktitle: Add Bidi Marks
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-txtsaveoptions/add-bidi-marks/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Hello world!");
            builder.ParagraphFormat.Bidi = true;
            builder.Writeln("שלום עולם!");
            builder.Writeln("مرحبا بالعالم!");

            TxtSaveOptions saveOptions = new TxtSaveOptions { AddBidiMarks = true };

            doc.Save(ArtifactsDir + "WorkingWithTxtSaveOptions.AddBidiMarks.txt", saveOptions);
            
        
```


---
title: Programming With Txtsaveoptions
linktitle: Programming With Txtsaveoptions
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain add bidi marks, use tab character per level for list indentation and use space character per level for list indentation
type: docs
weight: 1700
url: /words/net/programming-with-txtsaveoptions/
---
Tutorials contain add bidi marks, use tab character per level for list indentation and use space character per level for list indentation

## Add Bidi Marks

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

## Use Tab Character Per Level For List Indentation

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Create a list with three levels of indentation.
            builder.ListFormat.ApplyNumberDefault();
            builder.Writeln("Item 1");
            builder.ListFormat.ListIndent();
            builder.Writeln("Item 2");
            builder.ListFormat.ListIndent(); 
            builder.Write("Item 3");

            TxtSaveOptions saveOptions = new TxtSaveOptions();
            saveOptions.ListIndentation.Count = 1;
            saveOptions.ListIndentation.Character = '\t';

            doc.Save(ArtifactsDir + "WorkingWithTxtSaveOptions.UseTabCharacterPerLevelForListIndentation.txt", saveOptions);
            
        
```

## Use Space Character Per Level For List Indentation

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Create a list with three levels of indentation.
            builder.ListFormat.ApplyNumberDefault();
            builder.Writeln("Item 1");
            builder.ListFormat.ListIndent();
            builder.Writeln("Item 2");
            builder.ListFormat.ListIndent(); 
            builder.Write("Item 3");

            TxtSaveOptions saveOptions = new TxtSaveOptions();
            saveOptions.ListIndentation.Count = 3;
            saveOptions.ListIndentation.Character = ' ';

            doc.Save(ArtifactsDir + "WorkingWithTxtSaveOptions.UseSpaceCharacterPerLevelForListIndentation.txt", saveOptions);
            
        
```


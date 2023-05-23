---
title: Find And Replace Text
linktitle: Find And Replace Text
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain simple find replace, meta characters in search pattern, replace text containing meta characters, ignore text inside fields, ignore text inside 
type: docs
weight: 1360
url: /words/net/find-and-replace-text/
---
Tutorials contain simple find replace, meta characters in search pattern, replace text containing meta characters, ignore text inside fields, ignore text inside delete revisions, ignore text inside insert revisions, replace text in footer, replace with regex, recognize and substitutions within replacement patterns, replace with string and replace text in table

## Simple Find Replace

```csharp

            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Hello _CustomerName_,");
            Console.WriteLine("Original document text: " + doc.Range.Text);

            doc.Range.Replace("_CustomerName_", "James Bond", new FindReplaceOptions(FindReplaceDirection.Forward));

            Console.WriteLine("Document text after replace: " + doc.Range.Text);

            // Save the modified document
            doc.Save(ArtifactsDir + "FindAndReplace.SimpleFindReplace.docx");
        
```

## Meta Characters In Search Pattern

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

## Replace Text Containing Meta Characters

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
            int count = doc.Range.Replace("section&p", "section&p----------------------

 ## Tutorials
| Title | Description |
| --- | --- |
| [Simple Find Replace](./simple-find-replace/) | |
| [Meta Characters In Search Pattern](./meta-characters-in-search-pattern/) | |
| [Replace Text Containing Meta Characters](./replace-text-containing-meta-characters/) | |
| [Ignore Text Inside Fields](./ignore-text-inside-fields/) | |
| [Ignore Text Inside Delete Revisions](./ignore-text-inside-delete-revisions/) | |
| [Ignore Text Inside Insert Revisions](./ignore-text-inside-insert-revisions/) | |
| [Replace Text In Footer](./replace-text-in-footer/) | |
| [Replace With Regex](./replace-with-regex/) | |
| [Recognize And Substitutions Within Replacement Patterns](./recognize-and-substitutions-within-replacement-patterns/) | |
| [Replace With String](./replace-with-string/) | |
| [Replace Text In Table](./replace-text-in-table/) | |

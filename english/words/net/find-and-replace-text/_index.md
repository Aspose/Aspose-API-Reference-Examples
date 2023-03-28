---
title: Find And Replace Text
linktitle: Find And Replace Text
second_title: Aspose.Words for .NET API Reference
description: Examples contain simple find replace, meta characters in search pattern, replace text containing meta characters, ignore text inside fields, ignore text inside 
type: docs
weight: 1360
url: /words/net/find-and-replace-text/
---
Examples contain simple find replace, meta characters in search pattern, replace text containing meta characters, ignore text inside fields, ignore text inside delete revisions, ignore text inside insert revisions, replace text in footer, replace with regex, recognize and substitutions within replacement patterns, replace with string and replace text in table

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
            int count = doc.Range.Replace("section&p", "section&p----------------------&p", findReplaceOptions);

            // Insert section break instead of custom text tag.
            count = doc.Range.Replace("{insert-section}", "&b", findReplaceOptions);

            doc.Save(ArtifactsDir + "FindAndReplace.ReplaceTextContainingMetaCharacters.docx");
            
        
```

## Ignore Text Inside Fields

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Insert field with text inside.
            builder.InsertField("INCLUDETEXT", "Text in field");
            
            FindReplaceOptions options = new FindReplaceOptions { IgnoreFields = true };
            
            Regex regex = new Regex("e");
            doc.Range.Replace(regex, "*", options);
            
            Console.WriteLine(doc.GetText());

            options.IgnoreFields = false;
            doc.Range.Replace(regex, "*", options);
            
            Console.WriteLine(doc.GetText());
            
        
```

## Ignore Text Inside Delete Revisions

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Insert non-revised text.
            builder.Writeln("Deleted");
            builder.Write("Text");

            // Remove first paragraph with tracking revisions.
            doc.StartTrackRevisions("author", DateTime.Now);
            doc.FirstSection.Body.FirstParagraph.Remove();
            doc.StopTrackRevisions();

            FindReplaceOptions options = new FindReplaceOptions { IgnoreDeleted = true };

            Regex regex = new Regex("e");
            doc.Range.Replace(regex, "*", options);

            Console.WriteLine(doc.GetText());

            options.IgnoreDeleted = false;
            doc.Range.Replace(regex, "*", options);

            Console.WriteLine(doc.GetText());
            
        
```

## Ignore Text Inside Insert Revisions

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Insert text with tracking revisions.
            doc.StartTrackRevisions("author", DateTime.Now);
            builder.Writeln("Inserted");
            doc.StopTrackRevisions();

            // Insert non-revised text.
            builder.Write("Text");

            FindReplaceOptions options = new FindReplaceOptions { IgnoreInserted = true };

            Regex regex = new Regex("e");
            doc.Range.Replace(regex, "*", options);
            
            Console.WriteLine(doc.GetText());

            options.IgnoreInserted = false;
            doc.Range.Replace(regex, "*", options);
            
            Console.WriteLine(doc.GetText());
            
        
```

## Replace Text In Footer

```csharp

            
            Document doc = new Document(MyDir + "Footer.docx");

            HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
            HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

            FindReplaceOptions options = new FindReplaceOptions { MatchCase = false, FindWholeWordsOnly = false };

            footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", "Copyright (C) 2020 by Aspose Pty Ltd.", options);

            doc.Save(ArtifactsDir + "FindAndReplace.ReplaceTextInFooter.docx");
            
        
```

## Replace With Regex

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.Writeln("sad mad bad");

            FindReplaceOptions options = new FindReplaceOptions();

            doc.Range.Replace(new Regex("[s|m]ad"), "bad", options);

            doc.Save(ArtifactsDir + "FindAndReplace.ReplaceWithRegex.docx");
            
        
```

## Recognize And Substitutions Within Replacement Patterns

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Write("Jason give money to Paul.");

            Regex regex = new Regex(@"([A-z]+) give money to ([A-z]+)");

            FindReplaceOptions options = new FindReplaceOptions { UseSubstitutions = true };

            doc.Range.Replace(regex, @"$2 take money from $1", options);
            
        
```

## Replace With String

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.Writeln("sad mad bad");

            doc.Range.Replace("sad", "bad", new FindReplaceOptions(FindReplaceDirection.Forward));

            doc.Save(ArtifactsDir + "FindAndReplace.ReplaceWithString.docx");
            
        
```

## Replace Text In Table

```csharp

            
            Document doc = new Document(MyDir + "Tables.docx");

            Table table = (Table)doc.GetChild(NodeType.Table, 0, true);

            table.Range.Replace("Carrots", "Eggs", new FindReplaceOptions(FindReplaceDirection.Forward));
            table.LastRow.LastCell.Range.Replace("50", "20", new FindReplaceOptions(FindReplaceDirection.Forward));

            doc.Save(ArtifactsDir + "FindAndReplace.ReplaceTextInTable.docx");
            
        
```


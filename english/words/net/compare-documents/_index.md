---
title: Compare Documents
linktitle: Compare Documents
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain compare for equal, compare options, comparison target and comparison granularity
type: docs
weight: 1480
url: /words/net/compare-documents/
---
Tutorials contain compare for equal, compare options, comparison target and comparison granularity

## Compare For Equal

```csharp

            
            Document docA = new Document(MyDir + "Document.docx");
            Document docB = docA.Clone();
            
            // DocA now contains changes as revisions.
            docA.Compare(docB, "user", DateTime.Now);

            Console.WriteLine(docA.Revisions.Count == 0 ? "Documents are equal" : "Documents are not equal");
            
        
```

## Compare Options

```csharp

            
            Document docA = new Document(MyDir + "Document.docx");
            Document docB = docA.Clone();

            CompareOptions options = new CompareOptions
            {
                IgnoreFormatting = true,
                IgnoreHeadersAndFooters = true,
                IgnoreCaseChanges = true,
                IgnoreTables = true,
                IgnoreFields = true,
                IgnoreComments = true,
                IgnoreTextboxes = true,
                IgnoreFootnotes = true
            };

            docA.Compare(docB, "user", DateTime.Now, options);

            Console.WriteLine(docA.Revisions.Count == 0 ? "Documents are equal" : "Documents are not equal");
            
        
```

## Comparison Target

```csharp

            
            Document docA = new Document(MyDir + "Document.docx");
            Document docB = docA.Clone();

            // Relates to Microsoft Word "Show changes in" option in "Compare Documents" dialog box.
            CompareOptions options = new CompareOptions { IgnoreFormatting = true, Target = ComparisonTargetType.New };

            docA.Compare(docB, "user", DateTime.Now, options);
            
        
```

## Comparison Granularity

```csharp

            
            DocumentBuilder builderA = new DocumentBuilder(new Document());
            DocumentBuilder builderB = new DocumentBuilder(new Document());

            builderA.Writeln("This is A simple word");
            builderB.Writeln("This is B simple words");

            CompareOptions compareOptions = new CompareOptions { Granularity = Granularity.CharLevel };

            builderA.Document.Compare(builderB.Document, "author", DateTime.Now, compareOptions);
            
        
```


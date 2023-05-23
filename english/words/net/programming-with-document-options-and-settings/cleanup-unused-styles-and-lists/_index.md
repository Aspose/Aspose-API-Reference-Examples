---
title: Cleanup Unused Styles And Lists
linktitle: Cleanup Unused Styles And Lists
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-options-and-settings/cleanup-unused-styles-and-lists/
---




```csharp

            
            Document doc = new Document(MyDir + "Unused styles.docx");

            // Combined with the built-in styles, the document now has eight styles.
            // A custom style is marked as "used" while there is any text within the document
            // formatted in that style. This means that the 4 styles we added are currently unused.
            Console.WriteLine($"Count of styles before Cleanup: {doc.Styles.Count}\n" +
                              $"Count of lists before Cleanup: {doc.Lists.Count}");

            // Cleans unused styles and lists from the document depending on given CleanupOptions. 
            CleanupOptions cleanupOptions = new CleanupOptions { UnusedLists = false, UnusedStyles = true };
            doc.Cleanup(cleanupOptions);

            Console.WriteLine($"Count of styles after Cleanup was decreased: {doc.Styles.Count}\n" +
                              $"Count of lists after Cleanup is the same: {doc.Lists.Count}");

            doc.Save(ArtifactsDir + "WorkingWithDocumentOptionsAndSettings.CleanupUnusedStylesAndLists.docx");
            
        
```


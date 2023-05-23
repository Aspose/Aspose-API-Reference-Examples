---
title: Cleanup Duplicate Style
linktitle: Cleanup Duplicate Style
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-options-and-settings/cleanup-duplicate-style/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            // Count of styles before Cleanup.
            Console.WriteLine(doc.Styles.Count);

            // Cleans duplicate styles from the document.
            CleanupOptions options = new CleanupOptions { DuplicateStyle = true };
            doc.Cleanup(options);

            // Count of styles after Cleanup was decreased.
            Console.WriteLine(doc.Styles.Count);

            doc.Save(ArtifactsDir + "WorkingWithDocumentOptionsAndSettings.CleanupDuplicateStyle.docx");
            
        
```


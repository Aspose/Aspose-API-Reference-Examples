---
title: Insert Document At Replace
linktitle: Insert Document At Replace
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/clone-and-combine-documents/insert-document-at-replace/
---




```csharp

            
            Document mainDoc = new Document(MyDir + "Document insertion 1.docx");

            // Set find and replace options.
            FindReplaceOptions options = new FindReplaceOptions
            {
                Direction = FindReplaceDirection.Backward, 
                ReplacingCallback = new InsertDocumentAtReplaceHandler()
            };

            // Call the replace method.
            mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
            mainDoc.Save(ArtifactsDir + "CloneAndCombineDocuments.InsertDocumentAtReplace.docx");
            
        
```


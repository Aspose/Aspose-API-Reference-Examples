---
title: Clone And Combine Documents
linktitle: Clone And Combine Documents
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain cloning document, insert document at replace and insert document at mail merge
type: docs
weight: 1470
url: /words/net/clone-and-combine-documents/
---
Tutorials contain cloning document, insert document at replace and insert document at mail merge

## Cloning Document

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            Document clone = doc.Clone();
            clone.Save(ArtifactsDir + "CloneAndCombineDocuments.CloningDocument.docx");
            
        
```

## Insert Document At Replace

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

## Insert Document At Mail Merge

```csharp

            
            Document mainDoc = new Document(MyDir + "Document insertion 1.docx");

            mainDoc.MailMerge.FieldMergingCallback = new InsertDocumentAtMailMergeHandler();
            // The main document has a merge field in it called "Document_1".
            // The corresponding data for this field contains a fully qualified path to the document.
            // That should be inserted to this field.
            mainDoc.MailMerge.Execute(new[] { "Document_1" }, new object[] { MyDir + "Document insertion 2.docx" });

            mainDoc.Save(ArtifactsDir + "CloneAndCombineDocuments.InsertDocumentAtMailMerge.doc");
            
        
```


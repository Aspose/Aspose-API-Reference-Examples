---
title: Insert Document At Mail Merge
linktitle: Insert Document At Mail Merge
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/clone-and-combine-documents/insert-document-at-mail-merge/
---




```csharp

            
            Document mainDoc = new Document(MyDir + "Document insertion 1.docx");

            mainDoc.MailMerge.FieldMergingCallback = new InsertDocumentAtMailMergeHandler();
            // The main document has a merge field in it called "Document_1".
            // The corresponding data for this field contains a fully qualified path to the document.
            // That should be inserted to this field.
            mainDoc.MailMerge.Execute(new[] { "Document_1" }, new object[] { MyDir + "Document insertion 2.docx" });

            mainDoc.Save(ArtifactsDir + "CloneAndCombineDocuments.InsertDocumentAtMailMerge.doc");
            
        
```


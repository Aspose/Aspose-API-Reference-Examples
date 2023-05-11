---
title: Merge Documents
linktitle: Merge Documents
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/split-document/merge-documents/
---




```csharp

            // Find documents using for merge.
            FileSystemInfo[] documentPaths = new DirectoryInfo(ArtifactsDir)
                .GetFileSystemInfos("SplitDocument.PageByPage_*.docx").OrderBy(f => f.CreationTime).ToArray();
            string sourceDocumentPath =
                Directory.GetFiles(ArtifactsDir, "SplitDocument.PageByPage_1.docx", SearchOption.TopDirectoryOnly)[0];

            // Open the first part of the resulting document.
            Document sourceDoc = new Document(sourceDocumentPath);

            // Create a new resulting document.
            Document mergedDoc = new Document();
            DocumentBuilder mergedDocBuilder = new DocumentBuilder(mergedDoc);

            // Merge document parts one by one.
            foreach (FileSystemInfo documentPath in documentPaths)
            {
                if (documentPath.FullName == sourceDocumentPath)
                    continue;

                mergedDocBuilder.MoveToDocumentEnd();
                mergedDocBuilder.InsertDocument(sourceDoc, ImportFormatMode.KeepSourceFormatting);
                sourceDoc = new Document(documentPath.FullName);
            }

            mergedDoc.Save(ArtifactsDir + "SplitDocument.MergeDocuments.docx");
        
```


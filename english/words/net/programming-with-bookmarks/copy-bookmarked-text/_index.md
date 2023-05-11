---
title: Copy Bookmarked Text
linktitle: Copy Bookmarked Text
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-bookmarks/copy-bookmarked-text/
---




```csharp

            Document srcDoc = new Document(MyDir + "Bookmarks.docx");

            // This is the bookmark whose content we want to copy.
            Bookmark srcBookmark = srcDoc.Range.Bookmarks["MyBookmark1"];

            // We will be adding to this document.
            Document dstDoc = new Document();

            // Let's say we will be appended to the end of the body of the last section.
            CompositeNode dstNode = dstDoc.LastSection.Body;

            // If you import multiple times without a single context, it will result in many styles created.
            NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting);

            AppendBookmarkedText(importer, srcBookmark, dstNode);
            
            dstDoc.Save(ArtifactsDir + "WorkingWithBookmarks.CopyBookmarkedText.docx");
        
```


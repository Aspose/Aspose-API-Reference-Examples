---
title: Move To Node
linktitle: Move To Node
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/move-to-node/
---




```csharp

            
            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Start a bookmark and add content to it using a DocumentBuilder.
            builder.StartBookmark("MyBookmark");
            builder.Writeln("Bookmark contents.");
            builder.EndBookmark("MyBookmark");

            // The node that the DocumentBuilder is currently at is past the boundaries of the bookmark.
            Assert.AreEqual(doc.Range.Bookmarks[0].BookmarkEnd, builder.CurrentParagraph.FirstChild);

            // If we wish to revise the content of our bookmark with the DocumentBuilder, we can move back to it like this.
            builder.MoveToBookmark("MyBookmark");

            // Now we're located between the bookmark's BookmarkStart and BookmarkEnd nodes, so any text the builder adds will be within it.
            Assert.AreEqual(doc.Range.Bookmarks[0].BookmarkStart, builder.CurrentParagraph.FirstChild);

            // We can move the builder to an individual node,
            // which in this case will be the first node of the first paragraph, like this.
            builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);
            

            Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
            Assert.IsTrue(builder.IsAtStartOfParagraph);

            // A shorter way of moving the very start/end of a document is with these methods.
            builder.MoveToDocumentEnd();
            Assert.IsTrue(builder.IsAtEndOfParagraph);
            builder.MoveToDocumentStart();
            Assert.IsTrue(builder.IsAtStartOfParagraph);
            
        
```


---
title: Move Node In Tracked Document
linktitle: Move Node In Tracked Document
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-revisions/move-node-in-tracked-document/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);
	builder.Writeln("Paragraph 1");
	builder.Writeln("Paragraph 2");
	builder.Writeln("Paragraph 3");
	builder.Writeln("Paragraph 4");
	builder.Writeln("Paragraph 5");
	builder.Writeln("Paragraph 6");
	Body body = doc.FirstSection.Body;
	Console.WriteLine("Paragraph count: {0}", body.Paragraphs.Count);

	// Start tracking revisions.
	doc.StartTrackRevisions("Author", new DateTime(2020, 12, 23, 14, 0, 0));

	// Generate revisions when moving a node from one location to another.
	Node node = body.Paragraphs[3];
	Node endNode = body.Paragraphs[5].NextSibling;
	Node referenceNode = body.Paragraphs[0];
	while (node != endNode)
	{
		Node nextNode = node.NextSibling;
		body.InsertBefore(node, referenceNode);
		node = nextNode;
	}

	// Stop the process of tracking revisions.
	doc.StopTrackRevisions();

	// There are 3 additional paragraphs in the move-from range.
	Console.WriteLine("Paragraph count: {0}", body.Paragraphs.Count);
	doc.Save(ArtifactsDir + "WorkingWithRevisions.MoveNodeInTrackedDocument.docx");
            
```


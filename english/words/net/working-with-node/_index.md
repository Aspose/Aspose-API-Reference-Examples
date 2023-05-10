---
title: Working with Node
linktitle: Working with Node
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain how to use node type, get parent node, owner document, recursive all nodes, traverse all nodes, enumerate child nodes, and create paragraph nodes in Word Document using Aspose.Words for .NET.
type: docs
weight: 1000
url: /words/net/working-with-node/
---

The following tutorials contain how to use node type, get parent node, owner document, recursive all nodes, traverse all nodes, enumerate child nodes, and create paragraph nodes in Word Document using Aspose.Words for .NET.
## Use Node Type

```csharp
	Document doc = new Document();
	
	NodeType type = doc.NodeType;
            
```

## Get Parent Node

```csharp
	Document doc = new Document();

	// The section is the first child node of the document.
	Node section = doc.FirstChild;

	// The section's parent node is the document.
	Console.WriteLine("Section parent is the document: " + (doc == section.ParentNode));
            
```

## Owner Document

```csharp
	Document doc = new Document();

	// Creating a new node of any type requires a document passed into the constructor.
	Paragraph para = new Paragraph(doc);

	// The new paragraph node does not yet have a parent.
	Console.WriteLine("Paragraph has no parent node: " + (para.ParentNode == null));

	// But the paragraph node knows its document.
	Console.WriteLine("Both nodes' documents are the same: " + (para.Document == doc));

	// The fact that a node always belongs to a document allows us to access and modify
	// properties that reference the document-wide data, such as styles or lists.
	para.ParagraphFormat.StyleName = "Heading 1";

	// Now add the paragraph to the main text of the first section.
	doc.FirstSection.Body.AppendChild(para);

	// The paragraph node is now a child of the Body node.
	Console.WriteLine("Paragraph has a parent node: " + (para.ParentNode != null));
            
```

## Enumerate Child Nodes

```csharp
	Document doc = new Document();
	Paragraph paragraph = (Paragraph) doc.GetChild(NodeType.Paragraph, 0, true);

	NodeCollection children = paragraph.ChildNodes;
	foreach (Node child in children)
	{
		// A paragraph may contain children of various types such as runs, shapes, and others.
		if (child.NodeType == NodeType.Run)
		{
			Run run = (Run) child;
			Console.WriteLine(run.Text);
		}
	}
            
```

## Recurse All Nodes

```csharp
	Document doc = new Document(MyDir + "Paragraphs.docx");

	// Invoke the recursive function that will walk the tree.
	TraverseAllNodes(doc);
```

## Traverse All Nodes

```csharp
	// This is the most efficient way to loop through immediate children of a node.
	for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
	{
		Console.WriteLine(Node.NodeTypeToString(childNode.NodeType));

		// Recurse into the node if it is a composite node.
		if (childNode.IsComposite)
			TraverseAllNodes((CompositeNode) childNode);
	}
```

## Typed Access

```csharp
	Document doc = new Document();

	Section section = doc.FirstSection;
	Body body = section.Body;
	
	// Quick typed access to all Table child nodes contained in the Body.
	TableCollection tables = body.Tables;

	foreach (Table table in tables)
	{
		// Quick typed access to the first row of the table.
		table.FirstRow?.Remove();

		// Quick typed access to the last row of the table.
		table.LastRow?.Remove();
	}
            
```

## Create And Add Paragraph Node

```csharp
	Document doc = new Document();

	Paragraph para = new Paragraph(doc);

	Section section = doc.LastSection;
	section.Body.AppendChild(para);
            
```


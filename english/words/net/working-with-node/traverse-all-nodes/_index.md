---
title: Traverse All Nodes
linktitle: Traverse All Nodes
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-node/traverse-all-nodes/
---




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


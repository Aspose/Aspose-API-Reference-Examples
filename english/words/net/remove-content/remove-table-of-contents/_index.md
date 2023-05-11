---
title: Remove Table Of Contents
linktitle: Remove Table Of Contents
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/remove-content/remove-table-of-contents/
---




```csharp

            // Store the FieldStart nodes of TOC fields in the document for quick access.
            List<FieldStart> fieldStarts = new List<FieldStart>();
            // This is a list to store the nodes found inside the specified TOC. They will be removed at the end of this method.
            List<Node> nodeList = new List<Node>();

            foreach (FieldStart start in doc.GetChildNodes(NodeType.FieldStart, true))
            {
                if (start.FieldType == FieldType.FieldTOC)
                {
                    fieldStarts.Add(start);
                }
            }

            // Ensure the TOC specified by the passed index exists.
            if (index > fieldStarts.Count - 1)
                throw new ArgumentOutOfRangeException("TOC index is out of range");

            bool isRemoving = true;
            
            Node currentNode = fieldStarts[index];
            while (isRemoving)
            {
                // It is safer to store these nodes and delete them all at once later.
                nodeList.Add(currentNode);
                currentNode = currentNode.NextPreOrder(doc);

                // Once we encounter a FieldEnd node of type FieldTOC,
                // we know we are at the end of the current TOC and stop here.
                if (currentNode.NodeType == NodeType.FieldEnd)
                {
                    FieldEnd fieldEnd = (FieldEnd) currentNode;
                    if (fieldEnd.FieldType == FieldType.FieldTOC)
                        isRemoving = false;
                }
            }

            foreach (Node node in nodeList)
            {
                node.Remove();
            }
        
```


---
title: Insert Author Field
linktitle: Insert Author Field
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fields/insert-author-field/
---




```csharp
	Document doc = new Document();

	Paragraph para = (Paragraph) doc.GetChildNodes(NodeType.Paragraph, true)[0];

	// We want to insert an AUTHOR field like this:
	// { AUTHOR Test1 }

	FieldAuthor field = (FieldAuthor) para.AppendField(FieldType.FieldAuthor, false);            
	field.AuthorName = "Test1"; // { AUTHOR Test1 }

	field.Update();

	doc.Save(ArtifactsDir + "WorkingWithFields.InsertAuthorField.docx");
```


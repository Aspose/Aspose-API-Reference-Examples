---
title: Insert Ole Object With Ole Package
linktitle: Insert Ole Object With Ole Package
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-oleobjects-and-activex/insert-ole-object-with-ole-package/
---




```csharp
	Document doc = new Document();
	DocumentBuilder builder = new DocumentBuilder(doc);

	byte[] bs = File.ReadAllBytes(MyDir + "Zip file.zip");
	using (Stream stream = new MemoryStream(bs))
	{
		Shape shape = builder.InsertOleObject(stream, "Package", true, null);
		OlePackage olePackage = shape.OleFormat.OlePackage;
		olePackage.FileName = "filename.zip";
		olePackage.DisplayName = "displayname.zip";

		doc.Save(ArtifactsDir + "WorkingWithOleObjectsAndActiveX.InsertOleObjectWithOlePackage.docx");
	}
	

	
	Shape oleShape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
	byte[] oleRawData = oleShape.OleFormat.GetRawData();
            
```


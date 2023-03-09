---
title: Working with OleObjects and ActiveX
linktitle: Working with OleObjects and ActiveX
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 1080
url: /words/net/working-with-oleobjects-and-activex/
---

## Insert Ole Object

```csharp
        {
            //ExStart:DocumentBuilderInsertOleObject
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertOleObject("http://www.aspose.com", "htmlfile", true, true, null);

            doc.Save(ArtifactsDir + "WorkingWithOleObjectsAndActiveX.InsertOleObject.docx");
            //ExEnd:DocumentBuilderInsertOleObject
        }

```

## Insert Ole Object With Ole Package

```csharp
        {
            //ExStart:InsertOleObjectwithOlePackage
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
            //ExEnd:InsertOleObjectwithOlePackage

            //ExStart:GetAccessToOLEObjectRawData
            Shape oleShape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
            byte[] oleRawData = oleShape.OleFormat.GetRawData();
            //ExEnd:GetAccessToOLEObjectRawData
        }

```

## Insert Ole Object As Icon

```csharp
        {
            //ExStart:InsertOLEObjectAsIcon
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImagesDir + "Logo icon.ico",
                "My embedded file");

            doc.Save(ArtifactsDir + "WorkingWithOleObjectsAndActiveX.InsertOleObjectAsIcon.docx");
            //ExEnd:InsertOLEObjectAsIcon
        }

```

## Insert Ole Object As Icon Using Stream

```csharp
        {
            //ExStart:InsertOLEObjectAsIconUsingStream
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            using (MemoryStream stream = new MemoryStream(File.ReadAllBytes(MyDir + "Presentation.pptx")))
                builder.InsertOleObjectAsIcon(stream, "Package", ImagesDir + "Logo icon.ico", "My embedded file");

            doc.Save(ArtifactsDir + "WorkingWithOleObjectsAndActiveX.InsertOleObjectAsIconUsingStream.docx");
            //ExEnd:InsertOLEObjectAsIconUsingStream
        }

```

## Read Active XControl Properties

```csharp
        {
            Document doc = new Document(MyDir + "ActiveX controls.docx");

            string properties = "";
            foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true))
            {
                if (shape.OleFormat is null) break;

                OleControl oleControl = shape.OleFormat.OleControl;
                if (oleControl.IsForms2OleControl)
                {
                    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
                    properties = properties + "\nCaption: " + checkBox.Caption;
                    properties = properties + "\nValue: " + checkBox.Value;
                    properties = properties + "\nEnabled: " + checkBox.Enabled;
                    properties = properties + "\nType: " + checkBox.Type;
                    if (checkBox.ChildNodes != null)
                    {
                        properties = properties + "\nChildNodes: " + checkBox.ChildNodes;
                    }

                    properties += "\n";
                }
            }

            properties = properties + "\nTotal ActiveX Controls found: " + doc.GetChildNodes(NodeType.Shape, true).Count;
            Console.WriteLine("\n" + properties);
        }

```


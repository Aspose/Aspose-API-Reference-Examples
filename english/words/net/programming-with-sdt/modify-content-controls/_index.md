---
title: Modify Content Controls
linktitle: Modify Content Controls
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-sdt/modify-content-controls/
---
### Sample source code for Modify Content Controls using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Structured document tags.docx");
            foreach (StructuredDocumentTag sdt in doc.GetChildNodes(NodeType.StructuredDocumentTag, true))
            {
                switch (sdt.SdtType)
                {
                    case SdtType.PlainText:
                    {
                        sdt.RemoveAllChildren();
                        Paragraph para = sdt.AppendChild(new Paragraph(doc)) as Paragraph;
                        Run run = new Run(doc, "new text goes here");
                        para.AppendChild(run);
                        break;
                    }
                    case SdtType.DropDownList:
                    {
                        SdtListItem secondItem = sdt.ListItems[2];
                        sdt.ListItems.SelectedValue = secondItem;
                        break;
                    }
                    case SdtType.Picture:
                    {
                        Shape shape = (Shape) sdt.GetChild(NodeType.Shape, 0, true);
                        if (shape.HasImage)
                        {
                            shape.ImageData.SetImage(ImagesDir + "Watermark.png");
                        }
                        break;
                    }
                }
            }
            doc.Save(dataDir + "WorkingWithSdt.ModifyContentControls.docx");
```
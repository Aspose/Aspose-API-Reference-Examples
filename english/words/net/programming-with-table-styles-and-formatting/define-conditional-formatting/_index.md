---
title: Define Conditional Formatting
linktitle: Define Conditional Formatting
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-table-styles-and-formatting/define-conditional-formatting/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Table table = builder.StartTable();
            builder.InsertCell();
            builder.Write("Name");
            builder.InsertCell();
            builder.Write("Value");
            builder.EndRow();
            builder.InsertCell();
            builder.InsertCell();
            builder.EndTable();

            TableStyle tableStyle = (TableStyle) doc.Styles.Add(StyleType.Table, "MyTableStyle1");
            tableStyle.ConditionalStyles.FirstRow.Shading.BackgroundPatternColor = Color.GreenYellow;
            tableStyle.ConditionalStyles.FirstRow.Shading.Texture = TextureIndex.TextureNone;

            table.Style = tableStyle;

            doc.Save(ArtifactsDir + "WorkingWithTableStylesAndFormatting.DefineConditionalFormatting.docx");
            
        
```

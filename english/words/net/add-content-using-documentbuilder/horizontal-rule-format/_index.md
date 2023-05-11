---
title: Horizontal Rule Format
linktitle: Horizontal Rule Format
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/add-content-using-documentbuilder/horizontal-rule-format/
---




```csharp

            
            DocumentBuilder builder = new DocumentBuilder();

            Shape shape = builder.InsertHorizontalRule();
            
            HorizontalRuleFormat horizontalRuleFormat = shape.HorizontalRuleFormat;
            horizontalRuleFormat.Alignment = HorizontalRuleAlignment.Center;
            horizontalRuleFormat.WidthPercent = 70;
            horizontalRuleFormat.Height = 3;
            horizontalRuleFormat.Color = Color.Blue;
            horizontalRuleFormat.NoShade = true;

            builder.Document.Save(ArtifactsDir + "AddContentUsingDocumentBuilder.HorizontalRuleFormat.docx");
            
        
```


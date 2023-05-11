---
title: Math Equations
linktitle: Math Equations
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-officemath/math-equations/
---




```csharp

            
            Document doc = new Document(MyDir + "Office math.docx");
            OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

            // OfficeMath display type represents whether an equation is displayed inline with the text or displayed on its line.
            officeMath.DisplayType = OfficeMathDisplayType.Display;
            officeMath.Justification = OfficeMathJustification.Left;

            doc.Save(ArtifactsDir + "WorkingWithOfficeMath.MathEquations.docx");
            
        
```


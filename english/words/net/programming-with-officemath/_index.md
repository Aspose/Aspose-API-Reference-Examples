---
title: Programming With Officemath
linktitle: Programming With Officemath
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain math equations
type: docs
weight: 1550
url: /words/net/programming-with-officemath/
---
Tutorials contain math equations

## Math Equations

```csharp

            
            Document doc = new Document(MyDir + "Office math.docx");
            OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

            // OfficeMath display type represents whether an equation is displayed inline with the text or displayed on its line.
            officeMath.DisplayType = OfficeMathDisplayType.Display;
            officeMath.Justification = OfficeMathJustification.Left;

            doc.Save(ArtifactsDir + "WorkingWithOfficeMath.MathEquations.docx");
            
        
```


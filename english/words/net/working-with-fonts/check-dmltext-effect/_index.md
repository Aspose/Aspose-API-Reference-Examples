---
title: Check DMLText Effect
linktitle: Check DMLText Effect
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/check-dmltext-effect/
---




```csharp
            
            Document doc = new Document(MyDir + "DrawingML text effects.docx");
            
            RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
            Font runFont = runs[0].Font;

            // One run might have several Dml text effects applied.
            Console.WriteLine(runFont.HasDmlEffect(TextDmlEffect.Shadow));
            Console.WriteLine(runFont.HasDmlEffect(TextDmlEffect.Effect3D));
            Console.WriteLine(runFont.HasDmlEffect(TextDmlEffect.Reflection));
            Console.WriteLine(runFont.HasDmlEffect(TextDmlEffect.Outline));
            Console.WriteLine(runFont.HasDmlEffect(TextDmlEffect.Fill));
            
```


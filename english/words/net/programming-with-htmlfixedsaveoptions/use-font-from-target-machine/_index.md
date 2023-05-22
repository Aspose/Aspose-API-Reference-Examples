---
title: Use Font From Target Machine
linktitle: Use Font From Target Machine
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-htmlfixedsaveoptions/use-font-from-target-machine/
---




```csharp

            
            Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

            HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { UseTargetMachineFonts = true };

            doc.Save(ArtifactsDir + "WorkingWithHtmlFixedSaveOptions.UseFontFromTargetMachine.html", saveOptions);
            
        
```


---
title: Keep Legacy Control Chars
linktitle: Keep Legacy Control Chars
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-ooxmlsaveoptions/keep-legacy-control-chars/
---




```csharp

            
            Document doc = new Document(MyDir + "Legacy control character.doc");

            OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.FlatOpc) { KeepLegacyControlChars = true };

            doc.Save(ArtifactsDir + "WorkingWithOoxmlSaveOptions.KeepLegacyControlChars.docx", saveOptions);
            
        
```


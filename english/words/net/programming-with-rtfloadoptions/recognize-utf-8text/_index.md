---
title: Recognize Utf 8Text
linktitle: Recognize Utf 8Text
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-rtfloadoptions/recognize-utf-8text/
---




```csharp

            
            RtfLoadOptions loadOptions = new RtfLoadOptions { RecognizeUtf8Text = true };

            Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

            doc.Save(ArtifactsDir + "WorkingWithRtfLoadOptions.RecognizeUtf8Text.rtf");
            
        
```


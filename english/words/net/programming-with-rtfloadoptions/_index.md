---
title: Programming With Rtfloadoptions
linktitle: Programming With Rtfloadoptions
second_title: Aspose.Words for .NET API Reference
description: Examples contain recognize utf 8text
type: docs
weight: 1630
url: /words/net/programming-with-rtfloadoptions/
---
Examples contain recognize utf 8text

## Recognize Utf 8Text

```csharp

            
            RtfLoadOptions loadOptions = new RtfLoadOptions { RecognizeUtf8Text = true };

            Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

            doc.Save(ArtifactsDir + "WorkingWithRtfLoadOptions.RecognizeUtf8Text.rtf");
            
        
```


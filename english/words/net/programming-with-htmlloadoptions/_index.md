---
title: Programming With Htmlloadoptions
linktitle: Programming With Htmlloadoptions
second_title: Aspose.Words for .NET API Reference
description: Examples contain preferred control type
type: docs
weight: 1600
url: /words/net/programming-with-htmlloadoptions/
---
Examples contain preferred control type

## Preferred Control Type

```csharp

            
            const string html = @"
                <html>
                    <select name='ComboBox' size='1'>
                        <option value='val1'>item1</option>
                        <option value='val2'></option>                        
                    </select>
                </html>
            ";

            HtmlLoadOptions loadOptions = new HtmlLoadOptions { PreferredControlType = HtmlControlType.StructuredDocumentTag };

            Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

            doc.Save(ArtifactsDir + "WorkingWithHtmlLoadOptions.PreferredControlType.docx", SaveFormat.Docx);
            
        
```


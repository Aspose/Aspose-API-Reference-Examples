---
title: Preferred Control Type
linktitle: Preferred Control Type
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-htmlloadoptions/preferred-control-type/
---




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


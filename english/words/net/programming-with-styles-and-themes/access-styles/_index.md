---
title: Access Styles
linktitle: Access Styles
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-styles-and-themes/access-styles/
---




```csharp

            
            Document doc = new Document();

            string styleName = "";

            // Get styles collection from the document.
            StyleCollection styles = doc.Styles;
            foreach (Style style in styles)
            {
                if (styleName == "")
                {
                    styleName = style.Name;
                    Console.WriteLine(styleName);
                }
                else
                {
                    styleName = styleName + ", " + style.Name;
                    Console.WriteLine(styleName);
                }
            }
            
        
```


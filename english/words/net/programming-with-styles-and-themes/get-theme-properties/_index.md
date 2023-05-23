---
title: Get Theme Properties
linktitle: Get Theme Properties
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-styles-and-themes/get-theme-properties/
---




```csharp

            
            Document doc = new Document();

            Aspose.Words.Themes.Theme theme = doc.Theme;

            Console.WriteLine(theme.MajorFonts.Latin);
            Console.WriteLine(theme.MinorFonts.EastAsian);
            Console.WriteLine(theme.Colors.Accent1);
            
        
```


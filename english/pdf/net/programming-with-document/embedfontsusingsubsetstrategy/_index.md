---
title: Embed Fonts Using Subset Strategy
linktitle: Embed Fonts Using Subset Strategy
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 130
url: /pdf/net/programming-with-document/embedfontsusingsubsetstrategy/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";
            Document doc = new Document(dataDir + "input.pdf");
            // All fonts will be embedded as subset into document in case of SubsetAllFonts.
            doc.FontUtilities.SubsetFonts(FontSubsetStrategy.SubsetAllFonts);
            // Font subset will be embedded for fully embedded fonts but fonts which are not embedded into document will not be affected.
            doc.FontUtilities.SubsetFonts(FontSubsetStrategy.SubsetEmbeddedFontsOnly);
            doc.Save(dataDir + "Output_out.pdf");
            

        
```


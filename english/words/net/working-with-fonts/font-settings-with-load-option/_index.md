---
title: Font Settings With Load Option
linktitle: Font Settings With Load Option
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/font-settings-with-load-option/
---
### Sample source code for Font Settings With Load Option using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            LoadOptions loadOptions = new LoadOptions();
            loadOptions.FontSettings = new FontSettings();
            Document doc = new Document(dataDir + "Rendering.docx", loadOptions);
```
---
title: Docx To Markdown
linktitle: Docx To Markdown
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/basic-conversions/docx-to-markdown/
---




```csharp

            // The path to the documents directory.
			string dataDir = "YOUR DOCUMENT DIRECTORY";
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Some text!");

            doc.Save(dataDir + "BaseConversions.DocxToMarkdown.md");
            
        
```


---
title: Show Grammatical And Spelling Errors
linktitle: Show Grammatical And Spelling Errors
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-options-and-settings/show-grammatical-and-spelling-errors/
---




```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            doc.ShowGrammaticalErrors = true;
            doc.ShowSpellingErrors = true;

            doc.Save(ArtifactsDir + "WorkingWithDocumentOptionsAndSettings.ShowGrammaticalAndSpellingErrors.docx");
            
        
```


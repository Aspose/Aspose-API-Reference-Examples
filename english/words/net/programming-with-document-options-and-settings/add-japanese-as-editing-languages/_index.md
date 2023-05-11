---
title: Add Japanese As Editing Languages
linktitle: Add Japanese As Editing Languages
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-document-options-and-settings/add-japanese-as-editing-languages/
---




```csharp

            
            LoadOptions loadOptions = new LoadOptions();
            
            // Set language preferences that will be used when document is loading.
            loadOptions.LanguagePreferences.AddEditingLanguage(EditingLanguage.Japanese);
            

            Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

            int localeIdFarEast = doc.Styles.DefaultFont.LocaleIdFarEast;
            Console.WriteLine(
                localeIdFarEast == (int) EditingLanguage.Japanese
                    ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
                    : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
        
```


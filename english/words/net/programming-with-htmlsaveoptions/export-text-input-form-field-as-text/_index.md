---
title: Export Text Input Form Field As Text
linktitle: Export Text Input Form Field As Text
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-htmlsaveoptions/export-text-input-form-field-as-text/
---




```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            string imagesDir = Path.Combine(ArtifactsDir, "Images");

            // The folder specified needs to exist and should be empty.
            if (Directory.Exists(imagesDir))
                Directory.Delete(imagesDir, true);

            Directory.CreateDirectory(imagesDir);

            // Set an option to export form fields as plain text, not as HTML input elements.
            HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html)
            {
                ExportTextInputFormFieldAsText = true, ImagesFolder = imagesDir
            };

            doc.Save(ArtifactsDir + "WorkingWithHtmlSaveOptions.ExportTextInputFormFieldAsText.html", saveOptions);
            
        
```


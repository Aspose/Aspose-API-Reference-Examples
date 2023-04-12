---
title: Programming With Loadoptions
linktitle: Programming With Loadoptions
second_title: Aspose.Words for .NET API Reference
description: Examples contain update dirty fields, load encrypted document, convert shape to office math, set ms word version, use temp folder, warning callback, load with e
type: docs
weight: 1610
url: /words/net/programming-with-loadoptions/
---
Examples contain update dirty fields, load encrypted document, convert shape to office math, set ms word version, use temp folder, warning callback, load with encoding, skip pdf images, convert metafiles to png and load chm

## Update Dirty Fields

```csharp

            
            LoadOptions loadOptions = new LoadOptions { UpdateDirtyFields = true };

            Document doc = new Document(MyDir + "Dirty field.docx", loadOptions);

            doc.Save(ArtifactsDir + "WorkingWithLoadOptions.UpdateDirtyFields.docx");
            
        
```

## Load Encrypted Document

```csharp

            
            
            Document doc = new Document(MyDir + "Encrypted.docx", new LoadOptions("docPassword"));
            

            doc.Save(ArtifactsDir + "WorkingWithLoadOptions.LoadAndSaveEncryptedOdt.odt", new OdtSaveOptions("newPassword"));
            
        
```

## Convert Shape To Office Math

```csharp

            
            LoadOptions loadOptions = new LoadOptions { ConvertShapeToOfficeMath = true };

            Document doc = new Document(MyDir + "Office math.docx", loadOptions);

            doc.Save(ArtifactsDir + "WorkingWithLoadOptions.ConvertShapeToOfficeMath.docx", SaveFormat.Docx);
            
        
```

## Set Ms Word Version

```csharp

            
            // Create a new LoadOptions object, which will load documents according to MS Word 2019 specification by default
            // and change the loading version to Microsoft Word 2010.
            LoadOptions loadOptions = new LoadOptions { MswVersion = MsWordVersion.Word2010 };
            
            Document doc = new Document(MyDir + "Document.docx", loadOptions);

            doc.Save(ArtifactsDir + "WorkingWithLoadOptions.SetMsWordVersion.docx");
            
        
```

## Use Temp Folder

```csharp

            
            LoadOptions loadOptions = new LoadOptions { TempFolder = ArtifactsDir };

            Document doc = new Document(MyDir + "Document.docx", loadOptions);
            
        
```

## Warning Callback

```csharp

            
            LoadOptions loadOptions = new LoadOptions { WarningCallback = new DocumentLoadingWarningCallback() };
            
            Document doc = new Document(MyDir + "Document.docx", loadOptions);
            
        
```

## Load With Encoding

```csharp

            
            LoadOptions loadOptions = new LoadOptions { Encoding = Encoding.UTF7 };

            Document doc = new Document(MyDir + "Encoded in UTF-7.txt", loadOptions);
            
        
```

## Skip Pdf Images

```csharp

            
            PdfLoadOptions loadOptions = new PdfLoadOptions { SkipPdfImages = true };

            Document doc = new Document(MyDir + "Pdf Document.pdf", loadOptions);
            
        
```

## Convert Metafiles To Png

```csharp

            
            LoadOptions loadOptions = new LoadOptions { ConvertMetafilesToPng = true };

            Document doc = new Document(MyDir + "WMF with image.docx", loadOptions);
            
        
```

## Load Chm

```csharp

            
            LoadOptions loadOptions = new LoadOptions { Encoding = Encoding.GetEncoding("windows-1251") };

            Document doc = new Document(MyDir + "HTML help.chm", loadOptions);
            
        
```


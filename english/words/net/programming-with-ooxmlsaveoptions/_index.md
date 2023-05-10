---
title: Programming With Ooxmlsaveoptions
linktitle: Programming With Ooxmlsaveoptions
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain encrypt docx with password, ooxml compliance iso 29500_ 2008_ strict, update last saved time property, keep legacy control chars and set compre
type: docs
weight: 1660
url: /words/net/programming-with-ooxmlsaveoptions/
---
Tutorials contain encrypt docx with password, ooxml compliance iso 29500_ 2008_ strict, update last saved time property, keep legacy control chars and set compression level

## Encrypt Docx With Password

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "password" };

            doc.Save(ArtifactsDir + "WorkingWithOoxmlSaveOptions.EncryptDocxWithPassword.docx", saveOptions);
            
        
```

## Ooxml Compliance Iso 29500_ 2008_ Strict

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2016);
            
            OoxmlSaveOptions saveOptions = new OoxmlSaveOptions() { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

            doc.Save(ArtifactsDir + "WorkingWithOoxmlSaveOptions.OoxmlComplianceIso29500_2008_Strict.docx", saveOptions);
            
        
```

## Update Last Saved Time Property

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { UpdateLastSavedTimeProperty = true };

            doc.Save(ArtifactsDir + "WorkingWithOoxmlSaveOptions.UpdateLastSavedTimeProperty.docx", saveOptions);
            
        
```

## Keep Legacy Control Chars

```csharp

            
            Document doc = new Document(MyDir + "Legacy control character.doc");

            OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.FlatOpc) { KeepLegacyControlChars = true };

            doc.Save(ArtifactsDir + "WorkingWithOoxmlSaveOptions.KeepLegacyControlChars.docx", saveOptions);
            
        
```

## Set Compression Level

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { CompressionLevel = CompressionLevel.SuperFast };

            doc.Save(ArtifactsDir + "WorkingWithOoxmlSaveOptions.SetCompressionLevel.docx", saveOptions);
            
        
```


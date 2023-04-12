---
title: Programming With Docsaveoptions
linktitle: Programming With Docsaveoptions
second_title: Aspose.Words for .NET API Reference
description: Examples contain encrypt document with password, do not compress small metafiles and do not save picture bullet
type: docs
weight: 1600
url: /words/net/programming-with-docsaveoptions/
---
Examples contain encrypt document with password, do not compress small metafiles and do not save picture bullet

## Encrypt Document With Password

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.Write("Hello world!");

            DocSaveOptions saveOptions = new DocSaveOptions { Password = "password" };

            doc.Save(ArtifactsDir + "WorkingWithDocSaveOptions.EncryptDocumentWithPassword.docx", saveOptions);
            
        
```

## Do Not Compress Small Metafiles

```csharp

            
            Document doc = new Document(MyDir + "Microsoft equation object.docx");

            DocSaveOptions saveOptions = new DocSaveOptions { AlwaysCompressMetafiles = false };

            doc.Save(ArtifactsDir + "WorkingWithDocSaveOptions.NotCompressSmallMetafiles.docx", saveOptions);
            
        
```

## Do Not Save Picture Bullet

```csharp

            
            Document doc = new Document(MyDir + "Image bullet points.docx");

            DocSaveOptions saveOptions = new DocSaveOptions { SavePictureBullet = false };

            doc.Save(ArtifactsDir + "WorkingWithDocSaveOptions.DoNotSavePictureBullet.docx", saveOptions);
            
        
```


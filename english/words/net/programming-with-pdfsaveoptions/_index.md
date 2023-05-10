---
title: Programming With Pdfsaveoptions
linktitle: Programming With Pdfsaveoptions
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain display doc title in window titlebar, pdf render warnings, digitally signed pdf using certificate holder, embedded all fonts, embedded subset f
type: docs
weight: 1680
url: /words/net/programming-with-pdfsaveoptions/
---
Tutorials contain display doc title in window titlebar, pdf render warnings, digitally signed pdf using certificate holder, embedded all fonts, embedded subset fonts, disable embed windows fonts, skip embedded arial and times roman fonts, avoid embedding core fonts, escape uri, export header footer bookmarks, scale wmf fonts to metafile size, additional text positioning, conversion to pdf 17, downsampling images, set outline options, custom properties export, export document structure, image compression, update last printed property, dml 3deffects rendering and interpolate images

## Display Doc Title In Window Titlebar

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions { DisplayDocTitle = true };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.DisplayDocTitleInWindowTitlebar.pdf", saveOptions);
            
        
```

## Pdf Render Warnings

```csharp

            Document doc = new Document(MyDir + "WMF with image.docx");

            MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions
            {
                EmulateRasterOperations = false, RenderingMode = MetafileRenderingMode.VectorWithFallback
            };

            PdfSaveOptions saveOptions = new PdfSaveOptions { MetafileRenderingOptions = metafileRenderingOptions };

            // If Aspose.Words cannot correctly render some of the metafile records
            // to vector graphics then Aspose.Words renders this metafile to a bitmap.
            HandleDocumentWarnings callback = new HandleDocumentWarnings();
            doc.WarningCallback = callback;

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.PdfRenderWarnings.pdf", saveOptions);

            // While the file saves successfully, rendering warnings that occurred during saving are collected here.
            foreach (WarningInfo warningInfo in callback.mWarnings)
            {
                Console.WriteLine(warningInfo.Description);
            }
        
```

## Digitally Signed Pdf Using Certificate Holder

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.Writeln("Test Signed PDF.");

            PdfSaveOptions saveOptions = new PdfSaveOptions
            {
                DigitalSignatureDetails = new PdfDigitalSignatureDetails(
                    CertificateHolder.Create(MyDir + "morzal.pfx", "aw"), "reason", "location",
                    DateTime.Now)
            };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.DigitallySignedPdfUsingCertificateHolder.pdf", saveOptions);
            
        
```

## Embedded All Fonts

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            // The output PDF will be embedded with all fonts found in the document.
            PdfSaveOptions saveOptions = new PdfSaveOptions { EmbedFullFonts = true };
            
            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.EmbeddedFontsInPdf.pdf", saveOptions);
            
        
```

## Embedded Subset Fonts

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            // The output PDF will contain subsets of the fonts in the document.
            // Only the glyphs used in the document are included in the PDF fonts.
            PdfSaveOptions saveOptions = new PdfSaveOptions { EmbedFullFonts = false };
            
            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.EmbeddSubsetFonts.pdf", saveOptions);
            
        
```

## Disable Embed Windows Fonts

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            // The output PDF will be saved without embedding standard windows fonts.
            PdfSaveOptions saveOptions = new PdfSaveOptions { FontEmbeddingMode = PdfFontEmbeddingMode.EmbedNone };
            
            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.DisableEmbedWindowsFonts.pdf", saveOptions);
            
        
```

## Skip Embedded Arial And Times Roman Fonts

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions { FontEmbeddingMode = PdfFontEmbeddingMode.EmbedAll };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.SkipEmbeddedArialAndTimesRomanFonts.pdf", saveOptions);
            
        
```

## Avoid Embedding Core Fonts

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            // The output PDF will not be embedded with core fonts such as Arial, Times New Roman etc.
            PdfSaveOptions saveOptions = new PdfSaveOptions { UseCoreFonts = true };
            
            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.AvoidEmbeddingCoreFonts.pdf", saveOptions);
            
        
```

## Escape Uri

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.InsertHyperlink("Testlink", 
                "https://www.google.com/search?q=%2Fthe%20test", false);
            builder.Writeln();
            builder.InsertHyperlink("https://www.google.com/search?q=%2Fthe%20test", 
                "https://www.google.com/search?q=%2Fthe%20test", false);

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.EscapeUri.pdf");
            
        
```

## Export Header Footer Bookmarks

```csharp

            
            Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions();
            saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;
            saveOptions.HeaderFooterBookmarksExportMode = HeaderFooterBookmarksExportMode.First;

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.ExportHeaderFooterBookmarks.pdf", saveOptions);
            
        
```

## Scale Wmf Fonts To Metafile Size

```csharp

            
            Document doc = new Document(MyDir + "WMF with text.docx");

            MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions
            {
                ScaleWmfFontsToMetafileSize = false
            };

            // If Aspose.Words cannot correctly render some of the metafile records to vector graphics
            // then Aspose.Words renders this metafile to a bitmap.
            PdfSaveOptions saveOptions = new PdfSaveOptions { MetafileRenderingOptions = metafileRenderingOptions };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.ScaleWmfFontsToMetafileSize.pdf", saveOptions);
            
        
```

## Additional Text Positioning

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions { AdditionalTextPositioning = true };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
            
        
```

## Conversion To Pdf 17

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions { Compliance = PdfCompliance.Pdf17 };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.ConversionToPdf17.pdf", saveOptions);
            
        
```

## Downsampling Images

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            // We can set a minimum threshold for downsampling.
            // This value will prevent the second image in the input document from being downsampled.
            PdfSaveOptions saveOptions = new PdfSaveOptions
            {
                DownsampleOptions = { Resolution = 36, ResolutionThreshold = 128 }
            };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.DownsamplingImages.pdf", saveOptions);
            
        
```

## Set Outline Options

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions();
            saveOptions.OutlineOptions.HeadingsOutlineLevels = 3;
            saveOptions.OutlineOptions.ExpandedOutlineLevels = 1;

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.SetOutlineOptions.pdf", saveOptions);
            
        
```

## Custom Properties Export

```csharp

            
            Document doc = new Document();
            doc.CustomDocumentProperties.Add("Company", "Aspose");

            PdfSaveOptions saveOptions = new PdfSaveOptions { CustomPropertiesExport = PdfCustomPropertiesExport.Standard };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.CustomPropertiesExport.pdf", saveOptions);
            
        
```

## Export Document Structure

```csharp

            
            Document doc = new Document(MyDir + "Paragraphs.docx");

            // The file size will be increased and the structure will be visible in the "Content" navigation pane
            // of Adobe Acrobat Pro, while editing the .pdf.
            PdfSaveOptions saveOptions = new PdfSaveOptions { ExportDocumentStructure = true };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.ExportDocumentStructure.pdf", saveOptions);
            
        
```

## Image Compression

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions
            {
                ImageCompression = PdfImageCompression.Jpeg, PreserveFormFields = true
            };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.PdfImageCompression.pdf", saveOptions);

            PdfSaveOptions saveOptionsA2U = new PdfSaveOptions
            {
                Compliance = PdfCompliance.PdfA2u,
                ImageCompression = PdfImageCompression.Jpeg,
                JpegQuality = 100, // Use JPEG compression at 50% quality to reduce file size.
            };

            

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.PdfImageCompression_A2u.pdf", saveOptionsA2U);
            
        
```

## Update Last Printed Property

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions { UpdateLastPrintedProperty = true };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.UpdateIfLastPrinted.pdf", saveOptions);
            
        
```

## Dml 3DEffects Rendering

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions { Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.Dml3DEffectsRendering.pdf", saveOptions);
            
        
```

## Interpolate Images

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            PdfSaveOptions saveOptions = new PdfSaveOptions { InterpolateImages = true };

            doc.Save(ArtifactsDir + "WorkingWithPdfSaveOptions.InterpolateImages.pdf", saveOptions);
            
        
```


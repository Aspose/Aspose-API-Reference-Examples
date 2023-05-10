---
title: Join And Append Documents
linktitle: Join And Append Documents
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain simple append document, append document, append document to blank, append with import format options, different page setup, join continuous, jo
type: docs
weight: 1500
url: /words/net/join-and-append-documents/
---
Tutorials contain simple append document, append document, append document to blank, append with import format options, different page setup, join continuous, join new page, keep source formatting, keep source together, list keep source formatting, list use destination styles, restart page numbering, update page layout, use destination styles, smart style behavior, insert document with builder, keep source numbering, ignore text boxes, ignore header footer, link headers footers, remove source headers footers and unlink headers footers

## Simple Append Document

```csharp

            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Append the source document to the destination document using no extra options.
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.SimpleAppendDocument.docx");
        
```

## Append Document

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");
            
            // Loop through all sections in the source document.
            // Section nodes are immediate children of the Document node so we can just enumerate the Document.
            foreach (Section srcSection in srcDoc)
            {
                // Because we are copying a section from one document to another, 
                // it is required to import the Section node into the destination document.
                // This adjusts any document-specific references to styles, lists, etc.
                //
                // Importing a node creates a copy of the original node, but the copy
                // ss ready to be inserted into the destination document.
                Node dstSection = dstDoc.ImportNode(srcSection, true, ImportFormatMode.KeepSourceFormatting);

                // Now the new section node can be appended to the destination document.
                dstDoc.AppendChild(dstSection);
            }

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.AppendDocument.docx");
            
        
```

## Append Document To Blank

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document();
            
            // The destination document is not empty, often causing a blank page to appear before the appended document.
            // This is due to the base document having an empty section and the new document being started on the next page.
            // Remove all content from the destination document before appending.
            dstDoc.RemoveAllChildren();
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            
            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.AppendDocumentToBlank.docx");
            
        
```

## Append With Import Format Options

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source with list.docx");
            Document dstDoc = new Document(MyDir + "Document destination with list.docx");

            // Specify that if numbering clashes in source and destination documents,
            // then numbering from the source document will be used.
            ImportFormatOptions options = new ImportFormatOptions { KeepSourceNumbering = true };
            
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);
            
        
```

## Different Page Setup

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Set the source document to continue straight after the end of the destination document.
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.Continuous;

            // Restart the page numbering on the start of the source document.
            srcDoc.FirstSection.PageSetup.RestartPageNumbering = true;
            srcDoc.FirstSection.PageSetup.PageStartingNumber = 1;

            // To ensure this does not happen when the source document has different page setup settings, make sure the
            // settings are identical between the last section of the destination document.
            // If there are further continuous sections that follow on in the source document,
            // this will need to be repeated for those sections.
            srcDoc.FirstSection.PageSetup.PageWidth = dstDoc.LastSection.PageSetup.PageWidth;
            srcDoc.FirstSection.PageSetup.PageHeight = dstDoc.LastSection.PageSetup.PageHeight;
            srcDoc.FirstSection.PageSetup.Orientation = dstDoc.LastSection.PageSetup.Orientation;

            // Iterate through all sections in the source document.
            foreach (Paragraph para in srcDoc.GetChildNodes(NodeType.Paragraph, true))
            {
                para.ParagraphFormat.KeepWithNext = true;
            }

            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            
            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.DifferentPageSetup.docx");
            
        
```

## Join Continuous

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Make the document appear straight after the destination documents content.
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.Continuous;
            // Append the source document using the original styles found in the source document.
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            
            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.JoinContinuous.docx");
            
        
```

## Join New Page

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Set the appended document to start on a new page.
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.NewPage;
            // Append the source document using the original styles found in the source document.
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            
            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.JoinNewPage.docx");
            
        
```

## Keep Source Formatting

```csharp

            
            Document dstDoc = new Document();
            dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");

            Document srcDoc = new Document();
            srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");

            // Append the source document to the destination document.
            // Pass format mode to retain the original formatting of the source document when importing it.
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.KeepSourceFormatting.docx");
            
        
```

## Keep Source Together

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Document destination with list.docx");
            
            // Set the source document to appear straight after the destination document's content.
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.Continuous;

            foreach (Paragraph para in srcDoc.GetChildNodes(NodeType.Paragraph, true))
            {
                para.ParagraphFormat.KeepWithNext = true;
            }

            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            
            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.KeepSourceTogether.docx");
            
        
```

## List Keep Source Formatting

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Document destination with list.docx");

            // Append the content of the document so it flows continuously.
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.Continuous;

            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            
            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.ListKeepSourceFormatting.docx");
            
        
```

## List Use Destination Styles

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Document destination with list.docx");

            // Set the source document to continue straight after the end of the destination document.
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.Continuous;

            // Keep track of the lists that are created.
            Dictionary<int, Aspose.Words.Lists.List> newLists = new Dictionary<int, Aspose.Words.Lists.List>();

            foreach (Paragraph para in srcDoc.GetChildNodes(NodeType.Paragraph, true))
            {
                if (para.IsListItem)
                {
                    int listId = para.ListFormat.List.ListId;

                    // Check if the destination document contains a list with this ID already. If it does, then this may
                    // cause the two lists to run together. Create a copy of the list in the source document instead.
                    if (dstDoc.Lists.GetListByListId(listId) != null)
                    {
                        Aspose.Words.Lists.List currentList;
                        // A newly copied list already exists for this ID, retrieve the stored list,
                        // and use it on the current paragraph.
                        if (newLists.ContainsKey(listId))
                        {
                            currentList = newLists[listId];
                        }
                        else
                        {
                            // Add a copy of this list to the document and store it for later reference.
                            currentList = srcDoc.Lists.AddCopy(para.ListFormat.List);
                            newLists.Add(listId, currentList);
                        }

                        // Set the list of this paragraph to the copied list.
                        para.ListFormat.List = currentList;
                    }
                }
            }

            // Append the source document to end of the destination document.
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles);

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.ListUseDestinationStyles.docx");
            
        
```

## Restart Page Numbering

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.NewPage;
            srcDoc.FirstSection.PageSetup.RestartPageNumbering = true;

            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            
            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.RestartPageNumbering.docx");
            
        
```

## Update Page Layout

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // If the destination document is rendered to PDF, image etc.
            // or UpdatePageLayout is called before the source document. Is appended,
            // then any changes made after will not be reflected in the rendered output
            dstDoc.UpdatePageLayout();

            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);

            // For the changes to be updated to rendered output, UpdatePageLayout must be called again.
            // If not called again, the appended document will not appear in the output of the next rendering.
            dstDoc.UpdatePageLayout();

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.UpdatePageLayout.docx");
            
        
```

## Use Destination Styles

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Append the source document using the styles of the destination document.
            dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles);

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.UseDestinationStyles.docx");
            
        
```

## Smart Style Behavior

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");
            DocumentBuilder builder = new DocumentBuilder(dstDoc);
            
            builder.MoveToDocumentEnd();
            builder.InsertBreak(BreakType.PageBreak);

            ImportFormatOptions options = new ImportFormatOptions { SmartStyleBehavior = true };

            builder.InsertDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);
            builder.Document.Save(ArtifactsDir + "JoinAndAppendDocuments.SmartStyleBehavior.docx");
            
        
```

## Insert Document With Builder

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");
            DocumentBuilder builder = new DocumentBuilder(dstDoc);

            builder.MoveToDocumentEnd();
            builder.InsertBreak(BreakType.PageBreak);

            builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
            builder.Document.Save(ArtifactsDir + "JoinAndAppendDocuments.InsertDocumentWithBuilder.docx");
            
        
```

## Keep Source Numbering

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Keep source list formatting when importing numbered paragraphs.
            ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };
            
            NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting,
                importFormatOptions);

            ParagraphCollection srcParas = srcDoc.FirstSection.Body.Paragraphs;
            foreach (Paragraph srcPara in srcParas)
            {
                Node importedNode = importer.ImportNode(srcPara, false);
                dstDoc.FirstSection.Body.AppendChild(importedNode);
            }

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.KeepSourceNumbering.docx");
            
        
```

## Ignore Text Boxes

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Keep the source text boxes formatting when importing.
            ImportFormatOptions importFormatOptions = new ImportFormatOptions { IgnoreTextBoxes = false };
            
            NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting,
                importFormatOptions);

            ParagraphCollection srcParas = srcDoc.FirstSection.Body.Paragraphs;
            foreach (Paragraph srcPara in srcParas)
            {
                Node importedNode = importer.ImportNode(srcPara, true);
                dstDoc.FirstSection.Body.AppendChild(importedNode);
            }

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.IgnoreTextBoxes.docx");
            
        
```

## Ignore Header Footer

```csharp

            
            Document srcDocument = new Document(MyDir + "Document source.docx");
            Document dstDocument = new Document(MyDir + "Northwind traders.docx");

            ImportFormatOptions importFormatOptions = new ImportFormatOptions { IgnoreHeaderFooter = false };

            dstDocument.AppendDocument(srcDocument, ImportFormatMode.KeepSourceFormatting, importFormatOptions);
            
            dstDocument.Save(ArtifactsDir + "JoinAndAppendDocuments.IgnoreHeaderFooter.docx");
            
        
```

## Link Headers Footers

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Set the appended document to appear on a new page.
            srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.NewPage;
            // Link the headers and footers in the source document to the previous section.
            // This will override any headers or footers already found in the source document.
            srcDoc.FirstSection.HeadersFooters.LinkToPrevious(true);

            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.LinkHeadersFooters.docx");
            
        
```

## Remove Source Headers Footers

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Remove the headers and footers from each of the sections in the source document.
            foreach (Section section in srcDoc.Sections)
            {
                section.ClearHeadersFooters();
            }

            // Even after the headers and footers are cleared from the source document, the "LinkToPrevious" setting 
            // for HeadersFooters can still be set. This will cause the headers and footers to continue from the destination 
            // document. This should set to false to avoid this behavior.
            srcDoc.FirstSection.HeadersFooters.LinkToPrevious(false);

            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.RemoveSourceHeadersFooters.docx");
            
        
```

## Unlink Headers Footers

```csharp

            
            Document srcDoc = new Document(MyDir + "Document source.docx");
            Document dstDoc = new Document(MyDir + "Northwind traders.docx");

            // Unlink the headers and footers in the source document to stop this
            // from continuing the destination document's headers and footers.
            srcDoc.FirstSection.HeadersFooters.LinkToPrevious(false);

            dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);

            dstDoc.Save(ArtifactsDir + "JoinAndAppendDocuments.UnlinkHeadersFooters.docx");
            
        
```


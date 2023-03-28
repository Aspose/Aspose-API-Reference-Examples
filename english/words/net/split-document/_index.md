---
title: Split Document
linktitle: Split Document
second_title: Aspose.Words for .NET API Reference
description: Examples contain by headings html, by sections html, by sections, page by page, merge documents and by page range
type: docs
weight: 1450
url: /words/net/split-document/
---
Examples contain by headings html, by sections html, by sections, page by page, merge documents and by page range

## By Headings Html

```csharp

            
            Document doc = new Document(MyDir + "Rendering.docx");

            HtmlSaveOptions options = new HtmlSaveOptions
            {
                // Split a document into smaller parts, in this instance split by heading.
                DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph
            };
            

            doc.Save(ArtifactsDir + "SplitDocument.ByHeadingsHtml.html", options);
            
        
```

## By Sections Html

```csharp

            Document doc = new Document(MyDir + "Rendering.docx");
 
            
            HtmlSaveOptions options = new HtmlSaveOptions { DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak };
            
            
            doc.Save(ArtifactsDir + "SplitDocument.BySectionsHtml.html", options);
        
```

## By Sections

```csharp

            
            Document doc = new Document(MyDir + "Big document.docx");

            for (int i = 0; i < doc.Sections.Count; i++)
            {
                // Split a document into smaller parts, in this instance, split by section.
                Section section = doc.Sections[i].Clone();

                Document newDoc = new Document();
                newDoc.Sections.Clear();

                Section newSection = (Section) newDoc.ImportNode(section, true);
                newDoc.Sections.Add(newSection);

                // Save each section as a separate document.
                newDoc.Save(ArtifactsDir + $"SplitDocument.BySections_{i}.docx");
            }
            
        
```

## Page By Page

```csharp

            
            Document doc = new Document(MyDir + "Big document.docx");

            int pageCount = doc.PageCount;

            for (int page = 0; page < pageCount; page++)
            {
                // Save each page as a separate document.
                Document extractedPage = doc.ExtractPages(page, 1);
                extractedPage.Save(ArtifactsDir + $"SplitDocument.PageByPage_{page + 1}.docx");
            }
            

            MergeDocuments();
        
```

## Merge Documents

```csharp

            // Find documents using for merge.
            FileSystemInfo[] documentPaths = new DirectoryInfo(ArtifactsDir)
                .GetFileSystemInfos("SplitDocument.PageByPage_*.docx").OrderBy(f => f.CreationTime).ToArray();
            string sourceDocumentPath =
                Directory.GetFiles(ArtifactsDir, "SplitDocument.PageByPage_1.docx", SearchOption.TopDirectoryOnly)[0];

            // Open the first part of the resulting document.
            Document sourceDoc = new Document(sourceDocumentPath);

            // Create a new resulting document.
            Document mergedDoc = new Document();
            DocumentBuilder mergedDocBuilder = new DocumentBuilder(mergedDoc);

            // Merge document parts one by one.
            foreach (FileSystemInfo documentPath in documentPaths)
            {
                if (documentPath.FullName == sourceDocumentPath)
                    continue;

                mergedDocBuilder.MoveToDocumentEnd();
                mergedDocBuilder.InsertDocument(sourceDoc, ImportFormatMode.KeepSourceFormatting);
                sourceDoc = new Document(documentPath.FullName);
            }

            mergedDoc.Save(ArtifactsDir + "SplitDocument.MergeDocuments.docx");
        
```

## By Page Range

```csharp

            
            Document doc = new Document(MyDir + "Big document.docx");
            
            // Get part of the document.
            Document extractedPages = doc.ExtractPages(3, 6);
            extractedPages.Save(ArtifactsDir + "SplitDocument.ByPageRange.docx");
            
        
```


---
title: Export Into Markdown With Table Content Alignment
linktitle: Export Into Markdown With Table Content Alignment
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-markdownsaveoptions/export-into-markdown-with-table-content-alignment/
---




```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertCell();
            builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
            builder.Write("Cell1");
            builder.InsertCell();
            builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
            builder.Write("Cell2");

            // Makes all paragraphs inside the table to be aligned.
            MarkdownSaveOptions saveOptions = new MarkdownSaveOptions
            {
                TableContentAlignment = TableContentAlignment.Left
            };
            doc.Save(ArtifactsDir + "WorkingWithMarkdownSaveOptions.LeftTableContentAlignment.md", saveOptions);

            saveOptions.TableContentAlignment = TableContentAlignment.Right;
            doc.Save(ArtifactsDir + "WorkingWithMarkdownSaveOptions.RightTableContentAlignment.md", saveOptions);

            saveOptions.TableContentAlignment = TableContentAlignment.Center;
            doc.Save(ArtifactsDir + "WorkingWithMarkdownSaveOptions.CenterTableContentAlignment.md", saveOptions);

            // The alignment in this case will be taken from the first paragraph in corresponding table column.
            saveOptions.TableContentAlignment = TableContentAlignment.Auto;
            doc.Save(ArtifactsDir + "WorkingWithMarkdownSaveOptions.AutoTableContentAlignment.md", saveOptions);
            
        
```


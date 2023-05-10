---
title: Remove Content
linktitle: Remove Content
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain remove page breaks, remove page breaks, remove section breaks, remove footers, remove toc and remove table of contents
type: docs
weight: 1370
url: /words/net/remove-content/
---
Tutorials contain remove page breaks, remove page breaks, remove section breaks, remove footers, remove toc and remove table of contents

## Remove Page Breaks

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");
            

            // In Aspose.Words section breaks are represented as separate Section nodes in the document.
            // To remove these separate sections, the sections are combined.
            RemovePageBreaks(doc);
            RemoveSectionBreaks(doc);

            doc.Save(ArtifactsDir + "RemoveContent.RemovePageBreaks.docx");
        
```

## Remove Page Breaks

```csharp

            NodeCollection paragraphs = doc.GetChildNodes(NodeType.Paragraph, true);

            foreach (Paragraph para in paragraphs)
            {
                // If the paragraph has a page break before the set, then clear it.
                if (para.ParagraphFormat.PageBreakBefore)
                    para.ParagraphFormat.PageBreakBefore = false;

                // Check all runs in the paragraph for page breaks and remove them.
                foreach (Run run in para.Runs)
                {
                    if (run.Text.Contains(ControlChar.PageBreak))
                        run.Text = run.Text.Replace(ControlChar.PageBreak, string.Empty);
                }
            }
        
```

## Remove Section Breaks

```csharp

            // Loop through all sections starting from the section that precedes the last one and moving to the first section.
            for (int i = doc.Sections.Count - 2; i >= 0; i--)
            {
                // Copy the content of the current section to the beginning of the last section.
                doc.LastSection.PrependContent(doc.Sections[i]);
                // Remove the copied section.
                doc.Sections[i].Remove();
            }
        
```

## Remove Footers

```csharp

            
            Document doc = new Document(MyDir + "Header and footer types.docx");

            foreach (Section section in doc)
            {
                // Up to three different footers are possible in a section (for first, even and odd pages)
                // we check and delete all of them.
                HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
                footer?.Remove();

                // Primary footer is the footer used for odd pages.
                footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
                footer?.Remove();

                footer = section.HeadersFooters[HeaderFooterType.FooterEven];
                footer?.Remove();
            }

            doc.Save(ArtifactsDir + "RemoveContent.RemoveFooters.docx");
            
        
```

## Remove Toc

```csharp

            Document doc = new Document(MyDir + "Table of contents.docx");

            // Remove the first table of contents from the document.
            RemoveTableOfContents(doc, 0);

            doc.Save(ArtifactsDir + "RemoveContent.RemoveToc.doc");
        
```

## Remove Table Of Contents

```csharp

            // Store the FieldStart nodes of TOC fields in the document for quick access.
            List<FieldStart> fieldStarts = new List<FieldStart>();
            // This is a list to store the nodes found inside the specified TOC. They will be removed at the end of this method.
            List<Node> nodeList = new List<Node>();

            foreach (FieldStart start in doc.GetChildNodes(NodeType.FieldStart, true))
            {
                if (start.FieldType == FieldType.FieldTOC)
                {
                    fieldStarts.Add(start);
                }
            }

            // Ensure the TOC specified by the passed index exists.
            if (index > fieldStarts.Count - 1)
                throw new ArgumentOutOfRangeException("TOC index is out of range");

            bool isRemoving = true;
            
            Node currentNode = fieldStarts[index];
            while (isRemoving)
            {
                // It is safer to store these nodes and delete them all at once later.
                nodeList.Add(currentNode);
                currentNode = currentNode.NextPreOrder(doc);

                // Once we encounter a FieldEnd node of type FieldTOC,
                // we know we are at the end of the current TOC and stop here.
                if (currentNode.NodeType == NodeType.FieldEnd)
                {
                    FieldEnd fieldEnd = (FieldEnd) currentNode;
                    if (fieldEnd.FieldType == FieldType.FieldTOC)
                        isRemoving = false;
                }
            }

            foreach (Node node in nodeList)
            {
                node.Remove();
            }
        
```


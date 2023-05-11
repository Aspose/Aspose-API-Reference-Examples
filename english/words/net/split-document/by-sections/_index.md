---
title: By Sections
linktitle: By Sections
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/split-document/by-sections/
---




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


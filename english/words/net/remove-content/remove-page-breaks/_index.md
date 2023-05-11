---
title: Remove Page Breaks
linktitle: Remove Page Breaks
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/remove-content/remove-page-breaks/
---




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


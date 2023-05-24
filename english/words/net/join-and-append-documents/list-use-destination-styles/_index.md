---
title: List Use Destination Styles
linktitle: List Use Destination Styles
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/join-and-append-documents/list-use-destination-styles/
---
### Sample source code for List Use Destination Styles using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document srcDoc = new Document(dataDir + "Document source.docx");
            Document dstDoc = new Document(dataDir + "Document destination with list.docx");
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
            dstDoc.Save(dataDir + "JoinAndAppendDocuments.ListUseDestinationStyles.docx");
```
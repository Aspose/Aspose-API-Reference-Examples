---
title: Using Web Extension Task Panes
linktitle: Using Web Extension Task Panes
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-webextension/using-web-extension-task-panes/
---




```csharp

            
            Document doc = new Document();

            TaskPane taskPane = new TaskPane();
            doc.WebExtensionTaskPanes.Add(taskPane);

            taskPane.DockState = TaskPaneDockState.Right;
            taskPane.IsVisible = true;
            taskPane.Width = 300;

            taskPane.WebExtension.Reference.Id = "wa102923726";
            taskPane.WebExtension.Reference.Version = "1.0.0.0";
            taskPane.WebExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
            taskPane.WebExtension.Reference.Store = "th-TH";
            taskPane.WebExtension.Properties.Add(new WebExtensionProperty("mailchimpCampaign", "mailchimpCampaign"));
            taskPane.WebExtension.Bindings.Add(new WebExtensionBinding("UnnamedBinding_0_1506535429545",
                WebExtensionBindingType.Text, "194740422"));

            doc.Save(ArtifactsDir + "WorkingWithWebExtension.UsingWebExtensionTaskPanes.docx");
            
            
            
            doc = new Document(ArtifactsDir + "WorkingWithWebExtension.UsingWebExtensionTaskPanes.docx");
            
            Console.WriteLine("Task panes sources:\n");

            foreach (TaskPane taskPaneInfo in doc.WebExtensionTaskPanes)
            {
                WebExtensionReference reference = taskPaneInfo.WebExtension.Reference;
                Console.WriteLine($"Provider: \"{reference.Store}\", version: \"{reference.Version}\", catalog identifier: \"{reference.Id}\";");
            }
            
        
```


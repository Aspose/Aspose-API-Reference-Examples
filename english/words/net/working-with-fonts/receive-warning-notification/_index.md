---
title: Receive Warning Notification
linktitle: Receive Warning Notification
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/working-with-fonts/receive-warning-notification/
---
### Sample source code for Receive Warning Notification using Aspose.Words for .NET 
```csharp
// Path to your document directory 
string dataDir = "YOUR DOCUMENT DIRECTORY";

            Document doc = new Document(dataDir + "Rendering.docx");
            // When you call UpdatePageLayout the document is rendered in memory. Any warnings that occured during rendering
            // are stored until the document save and then sent to the appropriate WarningCallback.
            doc.UpdatePageLayout();
            HandleDocumentWarnings callback = new HandleDocumentWarnings();
            doc.WarningCallback = callback;
            // Even though the document was rendered previously, any save warnings are notified to the user during document save.
            doc.Save(dataDir + "WorkingWithFonts.ReceiveWarningNotification.pdf");
```
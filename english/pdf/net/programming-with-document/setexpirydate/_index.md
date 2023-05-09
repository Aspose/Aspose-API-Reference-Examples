---
title: Set Expiry Date
linktitle: Set Expiry Date
second_title: Aspose.PDF for .NET API Reference
description: 
type: docs
weight: 300
url: /pdf/net/programming-with-document/setexpirydate/
---



```csharp

            
            // The path to the documents directory.
            string dataDir = "YOUR DOCUMENT DIRECTORY";

            // Instantiate Document object
            Aspose.Pdf.Document doc = new Aspose.Pdf.Document();
            // Add page to pages collection of PDF file
            doc.Pages.Add();
            // Add text fragment to paragraphs collection of page object
            doc.Pages[1].Paragraphs.Add(new TextFragment("Hello World..."));
            // Create JavaScript object to set PDF expiry date
            JavascriptAction javaScript = new JavascriptAction(
            "var year=2017;"
            + "var month=5;"
            + "today = new Date(); today = new Date(today.getFullYear(), today.getMonth());"
            + "expiry = new Date(year, month);"
            + "if (today.getTime() > expiry.getTime())"
            + "app.alert('The file is expired. You need a new one.');");
            // Set JavaScript as PDF open action
            doc.OpenAction = javaScript;

            dataDir = dataDir + "SetExpiryDate_out.pdf";
            // Save PDF Document
            doc.Save(dataDir);
            
        
```


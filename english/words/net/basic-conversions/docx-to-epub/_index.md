---
title: Docx To Epub
linktitle: Docx To Epub
second_title: Aspose.Words for .NET API Reference
description: Learn how to convert Docx files to Epub format using Aspose.PDF for .NET with this comprehensive step-by-step guide.
type: docs
weight: 10
url: /words/net/basic-conversions/docx-to-epub/
---

## Step 1: Set the Document Directory
Before we begin, ensure that you have the Aspose.PDF for .NET library installed and referenced in your project. Set the `dataDir` variable to the directory path where your document is located. Update `"YOUR DOCUMENT DIRECTORY"` with the actual path to the directory containing your Docx file.

## Step 2: Load the Docx Document
To initiate the conversion, we need to load the Docx document into an Aspose.PDF `Document` object. Use the following code snippet to accomplish this:

```csharp
string dataDir = "YOUR DOCUMENT DIRECTORY";
Document doc = new Document(dataDir + "Document.docx");
```

Replace `"YOUR DOCUMENT DIRECTORY"` with the appropriate path to the directory where your Docx file is stored.

## Step 3: Convert Docx to Epub
Now, we can proceed with the conversion of the loaded Docx document to Epub format. Use the following code snippet to perform the conversion:

```csharp
doc.Save(dataDir + "BaseConversions.DocxToEpub.epub");
```

This code saves the converted Epub file to the specified path. Adjust the output file name and path (`dataDir + "BaseConversions.DocxToEpub.epub"`) according to your requirements.

Congratulations! You have successfully converted a Docx file to Epub format using Aspose.PDF for .NET.

### Example source code for Docx To Epub

		```csharp
		
		// The path to the documents directory.
		string dataDir = "YOUR DOCUMENT DIRECTORY";
		Document doc = new Document(dataDir + "Document.docx");

		doc.Save(dataDir + "BaseConversions.DocxToEpub.epub");
		
		```
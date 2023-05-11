---
title: Doc To Docx
linktitle: Doc To Docx
second_title: Aspose.Words for .NET API Reference
description: Learn how to convert DOC files to DOCX using Aspose.PDF for .NET. Step-by-step guide.
type: docs
weight: 10
url: /words/net/basic-conversions/doc-to-docx/
---
In this guide, we'll provide you with a step-by-step explanation of the C# source code to convert a DOC file to DOCX format using the Aspose.PDF for .NET library. By following these instructions, you'll be able to perform the conversion seamlessly in your own applications. Let's dive into the code!

## Step 1: Loading the Document

The first step is to load the source DOC document into a `Document` object. Replace `"YOUR DOCUMENT DIRECTORY"` with the actual directory path where your DOC file is located. The code snippet below demonstrates this step:

```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
Document doc = new Document(dataDir + "Document.doc");
```

## Step 2: Converting the Document to DOCX

Once the document is loaded, we can initiate the conversion process. Aspose.PDF for .NET provides a `Save` method that allows us to save the document in various formats, including DOCX. In this case, we'll convert the document to DOCX by specifying the output file name with the `.docx` extension. Here's the code snippet:

```csharp
doc.Save(dataDir + "BaseConversions.DocToDocx.docx");
```

## Step 3: Saving the Converted Document

Finally, we need to save the converted DOCX document to the desired location. Replace the directory path and file name with your preferred destination. Use the following code:

```csharp
doc.Save(dataDir + "ConvertedDocument.docx");
```

### Example Source Code for Doc To Docx using Aspose.PDF for .NET

```csharp

	// The path to the documents directory.
	string dataDir = "YOUR DOCUMENT DIRECTORY";
	Document doc = new Document(dataDir + "Document.doc");


	doc.Save(dataDir + "BaseConversions.DocToDocx.docx");

```
 
 
Remember to replace `"YOUR DOCUMENT DIRECTORY"` with the actual directory path specific to your system. Happy coding!






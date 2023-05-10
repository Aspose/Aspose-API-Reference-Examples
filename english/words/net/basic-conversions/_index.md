---
title: Basic Conversions
linktitle: Basic Conversions
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain doc to docx, docx to rtf, docx to pdf, docx to byte, docx to epub, docx to mhtml and sending email, docx to markdown, docx to txt, txt to docx,
type: docs
weight: 1600
url: /words/net/basic-conversions/
---
Tutorials contain doc to docx, docx to rtf, docx to pdf, docx to byte, docx to epub, docx to mhtml and sending email, docx to markdown, docx to txt, txt to docx, pdf to jpeg and pdf to docx

## Doc To Docx

```csharp

            
            
            Document doc = new Document(MyDir + "Document.doc");
            

            doc.Save(ArtifactsDir + "BaseConversions.DocToDocx.docx");
            
        
```

## Docx To Rtf

```csharp

            
            
            // Read only access is enough for Aspose.Words to load a document.
            Stream stream = File.OpenRead(MyDir + "Document.docx");

            Document doc = new Document(stream);
            // You can close the stream now, it is no longer needed because the document is in memory.
            stream.Close();
            

            // ... do something with the document.

            // Convert the document to a different format and save to stream.
            MemoryStream dstStream = new MemoryStream();
            doc.Save(dstStream, SaveFormat.Rtf);

            // Rewind the stream position back to zero so it is ready for the next reader.
            dstStream.Position = 0;
            
            
            File.WriteAllBytes(ArtifactsDir + "BaseConversions.DocxToRtf.rtf", dstStream.ToArray());
        
```

## Docx To Pdf

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            doc.Save(ArtifactsDir + "BaseConversions.DocxToPdf.pdf");
            
        
```

## Docx To Byte

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            MemoryStream outStream = new MemoryStream();
            doc.Save(outStream, SaveFormat.Docx);

            byte[] docBytes = outStream.ToArray();
            MemoryStream inStream = new MemoryStream(docBytes);

            Document docFromBytes = new Document(inStream);
            
        
```

## Docx To Epub

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            doc.Save(ArtifactsDir + "BaseConversions.DocxToEpub.epub");
            
        
```

## Docx To Mhtml And Sending Email

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            Stream stream = new MemoryStream();
            doc.Save(stream, SaveFormat.Mhtml);

            // Rewind the stream to the beginning so Aspose.Email can read it.
            stream.Position = 0;

            // Create an Aspose.Email MIME email message from the stream.
            MailMessage message = MailMessage.Load(stream, new MhtmlLoadOptions());
            message.From = "your_from@email.com";
            message.To = "your_to@email.com";
            message.Subject = "Aspose.Words + Aspose.Email MHTML Test Message";

            // Send the message using Aspose.Email.
            SmtpClient client = new SmtpClient();
            client.Host = "your_smtp.com";
            client.Send(message);
            
        
```

## Docx To Markdown

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Some text!");

            doc.Save(ArtifactsDir + "BaseConversions.DocxToMarkdown.md");
            
        
```

## Docx To Txt

```csharp

            
            Document doc = new Document(MyDir + "Document.docx");

            doc.Save(ArtifactsDir + "BaseConversions.DocxToTxt.txt");
            
        
```

## Txt To Docx

```csharp

            
            // The encoding of the text file is automatically detected.
            Document doc = new Document(MyDir + "English text.txt");

            doc.Save(ArtifactsDir + "BaseConversions.TxtToDocx.docx");
            
        
```

## Pdf To Jpeg

```csharp

            
            Document doc = new Document(MyDir + "Pdf Document.pdf");

            doc.Save(ArtifactsDir + "BaseConversions.PdfToJpeg.jpeg");
            
        
```

## Pdf To Docx

```csharp

            
            Document doc = new Document(MyDir + "Pdf Document.pdf");

            doc.Save(ArtifactsDir + "BaseConversions.PdfToDocx.docx");
            
        
```


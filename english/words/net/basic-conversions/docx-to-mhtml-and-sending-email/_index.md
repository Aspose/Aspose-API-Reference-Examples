---
title: Docx To Mhtml And Sending Email
linktitle: Docx To Mhtml And Sending Email
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/basic-conversions/docx-to-mhtml-and-sending-email/
---




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


---
title: Detect File Format
linktitle: Detect File Format
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 10
url: /words/net/programming-with-fileformat/detect-file-format/
---




```csharp

            
            string supportedDir = ArtifactsDir + "Supported";
            string unknownDir = ArtifactsDir + "Unknown";
            string encryptedDir = ArtifactsDir + "Encrypted";
            string pre97Dir = ArtifactsDir + "Pre97";

            // Create the directories if they do not already exist.
            if (Directory.Exists(supportedDir) == false)
                Directory.CreateDirectory(supportedDir);
            if (Directory.Exists(unknownDir) == false)
                Directory.CreateDirectory(unknownDir);
            if (Directory.Exists(encryptedDir) == false)
                Directory.CreateDirectory(encryptedDir);
            if (Directory.Exists(pre97Dir) == false)
                Directory.CreateDirectory(pre97Dir);

            
            IEnumerable<string> fileList = Directory.GetFiles(MyDir).Where(name => !name.EndsWith("Corrupted document.docx"));
            
            foreach (string fileName in fileList)
            {
                string nameOnly = Path.GetFileName(fileName);
                
                Console.Write(nameOnly);
                
                FileFormatInfo info = FileFormatUtil.DetectFileFormat(fileName);

                // Display the document type
                switch (info.LoadFormat)
                {
                    case LoadFormat.Doc:
                        Console.WriteLine("\tMicrosoft Word 97-2003 document.");
                        break;
                    case LoadFormat.Dot:
                        Console.WriteLine("\tMicrosoft Word 97-2003 template.");
                        break;
                    case LoadFormat.Docx:
                        Console.WriteLine("\tOffice Open XML WordprocessingML Macro-Free Document.");
                        break;
                    case LoadFormat.Docm:
                        Console.WriteLine("\tOffice Open XML WordprocessingML Macro-Enabled Document.");
                        break;
                    case LoadFormat.Dotx:
                        Console.WriteLine("\tOffice Open XML WordprocessingML Macro-Free Template.");
                        break;
                    case LoadFormat.Dotm:
                        Console.WriteLine("\tOffice Open XML WordprocessingML Macro-Enabled Template.");
                        break;
                    case LoadFormat.FlatOpc:
                        Console.WriteLine("\tFlat OPC document.");
                        break;
                    case LoadFormat.Rtf:
                        Console.WriteLine("\tRTF format.");
                        break;
                    case LoadFormat.WordML:
                        Console.WriteLine("\tMicrosoft Word 2003 WordprocessingML format.");
                        break;
                    case LoadFormat.Html:
                        Console.WriteLine("\tHTML format.");
                        break;
                    case LoadFormat.Mhtml:
                        Console.WriteLine("\tMHTML (Web archive) format.");
                        break;
                    case LoadFormat.Odt:
                        Console.WriteLine("\tOpenDocument Text.");
                        break;
                    case LoadFormat.Ott:
                        Console.WriteLine("\tOpenDocument Text Template.");
                        break;
                    case LoadFormat.DocPreWord60:
                        Console.WriteLine("\tMS Word 6 or Word 95 format.");
                        break;
                    case LoadFormat.Unknown:
                        Console.WriteLine("\tUnknown format.");
                        break;
                }
                

                if (info.IsEncrypted)
                {
                    Console.WriteLine("\tAn encrypted document.");
                    File.Copy(fileName, Path.Combine(encryptedDir, nameOnly), true);
                }
                else
                {
                    switch (info.LoadFormat)
                    {
                        case LoadFormat.DocPreWord60:
                            File.Copy(fileName, Path.Combine(pre97Dir, nameOnly), true);
                            break;
                        case LoadFormat.Unknown:
                            File.Copy(fileName, Path.Combine(unknownDir, nameOnly), true);
                            break;
                        default:
                            File.Copy(fileName, Path.Combine(supportedDir, nameOnly), true);
                            break;
                    }
                }
            }
            
        
```


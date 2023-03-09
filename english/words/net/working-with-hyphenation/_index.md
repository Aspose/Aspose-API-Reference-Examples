---
title: working with hyphenation
linktitle: working with hyphenation
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 750
url: /words/net/working-with-hyphenation/
---

## Hyphenate Words Of Languages

```csharp
        {
            //ExStart:HyphenateWordsOfLanguages
            Document doc = new Document(MyDir + "German text.docx");

            Hyphenation.RegisterDictionary("en-US", MyDir + "hyph_en_US.dic");
            Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

            doc.Save(ArtifactsDir + "WorkingWithHyphenation.HyphenateWordsOfLanguages.pdf");
            //ExEnd:HyphenateWordsOfLanguages
        }

```

## Load Hyphenation Dictionary For Language

```csharp
        {
            //ExStart:LoadHyphenationDictionaryForLanguage
            Document doc = new Document(MyDir + "German text.docx");
            
            Stream stream = File.OpenRead(MyDir + "hyph_de_CH.dic");
            Hyphenation.RegisterDictionary("de-CH", stream);

            doc.Save(ArtifactsDir + "WorkingWithHyphenation.LoadHyphenationDictionaryForLanguage.pdf");
            //ExEnd:LoadHyphenationDictionaryForLanguage
        }

```

## Hyphenation Callback

```csharp
        {
            try
            {
                // Register hyphenation callback.
                Hyphenation.Callback = new CustomHyphenationCallback();

                Document document = new Document(MyDir + "German text.docx");
                document.Save(ArtifactsDir + "WorkingWithHyphenation.HyphenationCallback.pdf");
            }
            catch (Exception e) when (e.Message.StartsWith("Missing hyphenation dictionary"))
            {
                Console.WriteLine(e.Message);
            }
            finally
            {
                Hyphenation.Callback = null;
            }
        }

```


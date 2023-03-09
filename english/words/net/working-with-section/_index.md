---
title: Working with Section
linktitle: Working with Section
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 1220
url: /words/net/working-with-section/
---

## Add Section

```csharp
        {
            //ExStart:AddSection
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Hello1");
            builder.Writeln("Hello2");

            Section sectionToAdd = new Section(doc);
            doc.Sections.Add(sectionToAdd);
            //ExEnd:AddSection
        }

```

## Delete Section

```csharp
        {
            //ExStart:DeleteSection
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Hello1");
            doc.AppendChild(new Section(doc));
            builder.Writeln("Hello2");
            doc.AppendChild(new Section(doc));

            doc.Sections.RemoveAt(0);
            //ExEnd:DeleteSection
        }

```

## Delete All Sections

```csharp
        {
            //ExStart:DeleteAllSections
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Hello1");
            doc.AppendChild(new Section(doc));
            builder.Writeln("Hello2");
            doc.AppendChild(new Section(doc));

            doc.Sections.Clear();
            //ExEnd:DeleteAllSections
        }

```

## Append Section Content

```csharp
        {
            //ExStart:AppendSectionContent
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Hello1");
            doc.AppendChild(new Section(doc));
            builder.Writeln("Hello22");
            doc.AppendChild(new Section(doc));
            builder.Writeln("Hello3");
            doc.AppendChild(new Section(doc));
            builder.Writeln("Hello45");

            // This is the section that we will append and prepend to.
            Section section = doc.Sections[2];

            // This copies the content of the 1st section and inserts it at the beginning of the specified section.
            Section sectionToPrepend = doc.Sections[0];
            section.PrependContent(sectionToPrepend);

            // This copies the content of the 2nd section and inserts it at the end of the specified section.
            Section sectionToAppend = doc.Sections[1];
            section.AppendContent(sectionToAppend);
            //ExEnd:AppendSectionContent
        }

```

## Clone Section

```csharp
        {
            //ExStart:CloneSection
            Document doc = new Document(MyDir + "Document.docx");
            Section cloneSection = doc.Sections[0].Clone();
            //ExEnd:CloneSection
        }

```

## Copy Section

```csharp
        {
            //ExStart:CopySection
            Document srcDoc = new Document(MyDir + "Document.docx");
            Document dstDoc = new Document();

            Section sourceSection = srcDoc.Sections[0];
            Section newSection = (Section) dstDoc.ImportNode(sourceSection, true);
            dstDoc.Sections.Add(newSection);
            
            dstDoc.Save(ArtifactsDir + "WorkingWithSection.CopySection.docx");
            //ExEnd:CopySection
        }

```

## Delete Header Footer Content

```csharp
        {
            //ExStart:DeleteHeaderFooterContent
            Document doc = new Document(MyDir + "Document.docx");
            
            Section section = doc.Sections[0];
            section.ClearHeadersFooters();
            //ExEnd:DeleteHeaderFooterContent
        }

```

## Delete Section Content

```csharp
        {
            //ExStart:DeleteSectionContent
            Document doc = new Document(MyDir + "Document.docx");
            
            Section section = doc.Sections[0];
            section.ClearContent();
            //ExEnd:DeleteSectionContent
        }

```

## Modify Page Setup In All Sections

```csharp
        {
            //ExStart:ModifyPageSetupInAllSections
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Writeln("Hello1");
            doc.AppendChild(new Section(doc));
            builder.Writeln("Hello22");
            doc.AppendChild(new Section(doc));
            builder.Writeln("Hello3");
            doc.AppendChild(new Section(doc));
            builder.Writeln("Hello45");

            // It is important to understand that a document can contain many sections,
            // and each section has its page setup. In this case, we want to modify them all.
            foreach (Section section in doc)
                section.PageSetup.PaperSize = PaperSize.Letter;

            doc.Save(ArtifactsDir + "WorkingWithSection.ModifyPageSetupInAllSections.doc");
            //ExEnd:ModifyPageSetupInAllSections
        }

```

## Sections Access By Index

```csharp
        {
            //ExStart:SectionsAccessByIndex
            Document doc = new Document(MyDir + "Document.docx");
            
            Section section = doc.Sections[0];
            section.PageSetup.LeftMargin = 90; // 3.17 cm
            section.PageSetup.RightMargin = 90; // 3.17 cm
            section.PageSetup.TopMargin = 72; // 2.54 cm
            section.PageSetup.BottomMargin = 72; // 2.54 cm
            section.PageSetup.HeaderDistance = 35.4; // 1.25 cm
            section.PageSetup.FooterDistance = 35.4; // 1.25 cm
            section.PageSetup.TextColumns.Spacing = 35.4; // 1.25 cm
            //ExEnd:SectionsAccessByIndex
        }

```


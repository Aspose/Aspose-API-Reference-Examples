---
title: working with fields
linktitle: working with fields
second_title: Aspose.Words for .NET API Reference
description:
type: docs
weight: 140
url: /words/net/working-with-fields/
---

## Field Code

```csharp
        {
            Document doc = new Document(MyDir + "Hyperlinks.docx");

            foreach (Field field in doc.Range.Fields)
            {
                string fieldCode = field.GetFieldCode();
                string fieldResult = field.Result;
            }
        }

```

## Change Field Update Culture Source

```csharp
        {
            //ExStart:ChangeFieldUpdateCultureSource
            //ExStart:DocumentBuilderInsertField
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Insert content with German locale.
            builder.Font.LocaleId = 1031;
            builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
            builder.Write(" - ");
            builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");
            //ExEnd:DocumentBuilderInsertField

            // Shows how to specify where the culture used for date formatting during field update and mail merge is chosen from
            // set the culture used during field update to the culture used by the field.
            doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
            doc.MailMerge.Execute(new string[] { "Date2" }, new object[] { new DateTime(2011, 1, 01) });
            
            doc.Save(ArtifactsDir + "WorkingWithFields.ChangeFieldUpdateCultureSource.docx");
            //ExEnd:ChangeFieldUpdateCultureSource
        }

```

## Specify Locale At Field Level

```csharp
        {
            //ExStart:SpecifylocaleAtFieldlevel
            DocumentBuilder builder = new DocumentBuilder();

            Field field = builder.InsertField(FieldType.FieldDate, true);
            field.LocaleId = 1049;
            
            builder.Document.Save(ArtifactsDir + "WorkingWithFields.SpecifylocaleAtFieldlevel.docx");
            //ExEnd:SpecifylocaleAtFieldlevel
        }

```

## Replace Hyperlinks

```csharp
        {
            //ExStart:ReplaceHyperlinks
            Document doc = new Document(MyDir + "Hyperlinks.docx");

            foreach (Field field in doc.Range.Fields)
            {
                if (field.Type == FieldType.FieldHyperlink)
                {
                    FieldHyperlink hyperlink = (FieldHyperlink) field;

                    // Some hyperlinks can be local (links to bookmarks inside the document), ignore these.
                    if (hyperlink.SubAddress != null)
                        continue;

                    hyperlink.Address = "http://www.aspose.com";
                    hyperlink.Result = "Aspose - The .NET & Java Component Publisher";
                }
            }

            doc.Save(ArtifactsDir + "WorkingWithFields.ReplaceHyperlinks.docx");
            //ExEnd:ReplaceHyperlinks
        }

```

## Rename Merge Fields

```csharp
        {
            //ExStart:RenameMergeFields
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
            builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

            foreach (Field f in doc.Range.Fields)
            {
                if (f.Type == FieldType.FieldMergeField)
                {
                    FieldMergeField mergeField = (FieldMergeField)f;
                    mergeField.FieldName = mergeField.FieldName + "_Renamed";
                    mergeField.Update();
                }
            }

            doc.Save(ArtifactsDir + "WorkingWithFields.RenameMergeFields.docx");
            //ExEnd:RenameMergeFields
        }

```

## Remove Field

```csharp
        {
            //ExStart:RemoveField
            Document doc = new Document(MyDir + "Various fields.docx");
            
            Field field = doc.Range.Fields[0];
            field.Remove();
            //ExEnd:RemoveField
        }

```

## Unlink Fields

```csharp
        {
            //ExStart:UnlinkFields
            Document doc = new Document(MyDir + "Various fields.docx");
            doc.UnlinkFields();
            //ExEnd:UnlinkFields
        }

```

## Insert TOAField Without Document Builder

```csharp
        {
            //ExStart:InsertTOAFieldWithoutDocumentBuilder
            Document doc = new Document();
            Paragraph para = new Paragraph(doc);

            // We want to insert TA and TOA fields like this:
            // { TA  \c 1 \l "Value 0" }
            // { TOA  \c 1 }

            FieldTA fieldTA = (FieldTA) para.AppendField(FieldType.FieldTOAEntry, false);
            fieldTA.EntryCategory = "1";
            fieldTA.LongCitation = "Value 0";

            doc.FirstSection.Body.AppendChild(para);

            para = new Paragraph(doc);

            FieldToa fieldToa = (FieldToa) para.AppendField(FieldType.FieldTOA, false);
            fieldToa.EntryCategory = "1";
            doc.FirstSection.Body.AppendChild(para);

            fieldToa.Update();

            doc.Save(ArtifactsDir + "WorkingWithFields.InsertTOAFieldWithoutDocumentBuilder.docx");
            //ExEnd:InsertTOAFieldWithoutDocumentBuilder
        }

```

## Insert Nested Fields

```csharp
        {
            //ExStart:InsertNestedFields
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            for (int i = 0; i < 5; i++)
                builder.InsertBreak(BreakType.PageBreak);

            builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);

            // We want to insert a field like this:
            // { IF {PAGE} <> {NUMPAGES} "See Next Page" "Last Page" }
            Field field = builder.InsertField(@"IF ");
            builder.MoveTo(field.Separator);
            builder.InsertField("PAGE");
            builder.Write(" <> ");
            builder.InsertField("NUMPAGES");
            builder.Write(" \"See Next Page\" \"Last Page\" ");

            field.Update();

            doc.Save(ArtifactsDir + "WorkingWithFields.InsertNestedFields.docx");
            //ExEnd:InsertNestedFields
        }

```

## Insert Merge Field Using DOM

```csharp
        {
            //ExStart:InsertMergeFieldUsingDOM
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Paragraph para = (Paragraph) doc.GetChildNodes(NodeType.Paragraph, true)[0];

            builder.MoveTo(para);

            // We want to insert a merge field like this:
            // { " MERGEFIELD Test1 \\b Test2 \\f Test3 \\m \\v" }

            FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, false);

            // { " MERGEFIELD Test1" }
            field.FieldName = "Test1";

            // { " MERGEFIELD Test1 \\b Test2" }
            field.TextBefore = "Test2";

            // { " MERGEFIELD Test1 \\b Test2 \\f Test3 }
            field.TextAfter = "Test3";

            // { " MERGEFIELD Test1 \\b Test2 \\f Test3 \\m" }
            field.IsMapped = true;

            // { " MERGEFIELD Test1 \\b Test2 \\f Test3 \\m \\v" }
            field.IsVerticalFormatting = true;

            // Finally update this merge field
            field.Update();

            doc.Save(ArtifactsDir + "WorkingWithFields.InsertMergeFieldUsingDOM.docx");
            //ExEnd:InsertMergeFieldUsingDOM
        }

```

## Insert Mail Merge Address Block Field Using DOM

```csharp
        {
            //ExStart:InsertMailMergeAddressBlockFieldUsingDOM
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Paragraph para = (Paragraph) doc.GetChildNodes(NodeType.Paragraph, true)[0];

            builder.MoveTo(para);

            // We want to insert a mail merge address block like this:
            // { ADDRESSBLOCK \\c 1 \\d \\e Test2 \\f Test3 \\l \"Test 4\" }

            FieldAddressBlock field = (FieldAddressBlock) builder.InsertField(FieldType.FieldAddressBlock, false);

            // { ADDRESSBLOCK \\c 1" }
            field.IncludeCountryOrRegionName = "1";

            // { ADDRESSBLOCK \\c 1 \\d" }
            field.FormatAddressOnCountryOrRegion = true;

            // { ADDRESSBLOCK \\c 1 \\d \\e Test2 }
            field.ExcludedCountryOrRegionName = "Test2";

            // { ADDRESSBLOCK \\c 1 \\d \\e Test2 \\f Test3 }
            field.NameAndAddressFormat = "Test3";

            // { ADDRESSBLOCK \\c 1 \\d \\e Test2 \\f Test3 \\l \"Test 4\" }
            field.LanguageId = "Test 4";

            field.Update();

            doc.Save(ArtifactsDir + "WorkingWithFields.InsertMailMergeAddressBlockFieldUsingDOM.docx");
            //ExEnd:InsertMailMergeAddressBlockFieldUsingDOM
        }

```

## Insert Field Include Text Without Document Builder

```csharp
        {
            //ExStart:InsertFieldIncludeTextWithoutDocumentBuilder
            Document doc = new Document();

            Paragraph para = new Paragraph(doc);

            // We want to insert an INCLUDETEXT field like this:
            // { INCLUDETEXT  "file path" }

            FieldIncludeText fieldIncludeText = (FieldIncludeText) para.AppendField(FieldType.FieldIncludeText, false);
            fieldIncludeText.BookmarkName = "bookmark";
            fieldIncludeText.SourceFullName = MyDir + "IncludeText.docx";

            doc.FirstSection.Body.AppendChild(para);

            fieldIncludeText.Update();

            doc.Save(ArtifactsDir + "WorkingWithFields.InsertIncludeFieldWithoutDocumentBuilder.docx");
            //ExEnd:InsertFieldIncludeTextWithoutDocumentBuilder
        }

```

## Insert Field None

```csharp
        {
            //ExStart:InsertFieldNone
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            FieldUnknown field = (FieldUnknown) builder.InsertField(FieldType.FieldNone, false);

            doc.Save(ArtifactsDir + "WorkingWithFields.InsertFieldNone.docx");
            //ExEnd:InsertFieldNone
        }

```

## Insert Field

```csharp
        {
            //ExStart:InsertField
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            
            builder.InsertField(@"MERGEFIELD MyFieldName \* MERGEFORMAT");
            
            doc.Save(ArtifactsDir + "WorkingWithFields.InsertField.docx");
            //ExEnd:InsertField
        }

```

## Insert Field Using Field Builder

```csharp
        {
            Document doc = new Document();

            // Prepare IF field with two nested MERGEFIELD fields: { IF "left expression" = "right expression" "Firstname: { MERGEFIELD firstname }" "Lastname: { MERGEFIELD lastname }"}
            FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldIf)
                .AddArgument("left expression")
                .AddArgument("=")
                .AddArgument("right expression")
                .AddArgument(
                    new FieldArgumentBuilder()
                        .AddText("Firstname: ")
                        .AddField(new FieldBuilder(FieldType.FieldMergeField).AddArgument("firstname")))
                .AddArgument(
                    new FieldArgumentBuilder()
                        .AddText("Lastname: ")
                        .AddField(new FieldBuilder(FieldType.FieldMergeField).AddArgument("lastname")));

            // Insert IF field in exact location            
            Field field = fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);
            field.Update();

            doc.Save(ArtifactsDir + "Field.InsertFieldUsingFieldBuilder.docx");
        }

```

## Insert Author Field

```csharp
        {
            //ExStart:InsertAuthorField
            Document doc = new Document();

            Paragraph para = (Paragraph) doc.GetChildNodes(NodeType.Paragraph, true)[0];

            // We want to insert an AUTHOR field like this:
            // { AUTHOR Test1 }

            FieldAuthor field = (FieldAuthor) para.AppendField(FieldType.FieldAuthor, false);            
            field.AuthorName = "Test1"; // { AUTHOR Test1 }

            field.Update();

            doc.Save(ArtifactsDir + "WorkingWithFields.InsertAuthorField.docx");
            //ExEnd:InsertAuthorField
        }

```

## Insert ASKField With Out Document Builder

```csharp
        {
            //ExStart:InsertASKFieldWithOutDocumentBuilder
            Document doc = new Document();

            Paragraph para = (Paragraph) doc.GetChildNodes(NodeType.Paragraph, true)[0];

            // We want to insert an Ask field like this:
            // { ASK \"Test 1\" Test2 \\d Test3 \\o }

            FieldAsk field = (FieldAsk) para.AppendField(FieldType.FieldAsk, false);

            // { ASK \"Test 1\" " }
            field.BookmarkName = "Test 1";

            // { ASK \"Test 1\" Test2 }
            field.PromptText = "Test2";

            // { ASK \"Test 1\" Test2 \\d Test3 }
            field.DefaultResponse = "Test3";

            // { ASK \"Test 1\" Test2 \\d Test3 \\o }
            field.PromptOnceOnMailMerge = true;

            field.Update();

            doc.Save(ArtifactsDir + "WorkingWithFields.InsertASKFieldWithOutDocumentBuilder.docx");
            //ExEnd:InsertASKFieldWithOutDocumentBuilder
        }

```

## Insert Advance Field With Out Document Builder

```csharp
        {
            //ExStart:InsertAdvanceFieldWithOutDocumentBuilder
            Document doc = new Document();

            Paragraph para = (Paragraph) doc.GetChildNodes(NodeType.Paragraph, true)[0];

            // We want to insert an Advance field like this:
            // { ADVANCE \\d 10 \\l 10 \\r -3.3 \\u 0 \\x 100 \\y 100 }

            FieldAdvance field = (FieldAdvance) para.AppendField(FieldType.FieldAdvance, false);
            
            // { ADVANCE \\d 10 " }
            field.DownOffset = "10";

            // { ADVANCE \\d 10 \\l 10 }
            field.LeftOffset = "10";

            // { ADVANCE \\d 10 \\l 10 \\r -3.3 }
            field.RightOffset = "-3.3";

            // { ADVANCE \\d 10 \\l 10 \\r -3.3 \\u 0 }
            field.UpOffset = "0";

            // { ADVANCE \\d 10 \\l 10 \\r -3.3 \\u 0 \\x 100 }
            field.HorizontalPosition = "100";

            // { ADVANCE \\d 10 \\l 10 \\r -3.3 \\u 0 \\x 100 \\y 100 }
            field.VerticalPosition = "100";

            field.Update();

            doc.Save(ArtifactsDir + "WorkingWithFields.InsertAdvanceFieldWithOutDocumentBuilder.docx");
            //ExEnd:InsertAdvanceFieldWithOutDocumentBuilder
        }

```

## Get Mail Merge Field Names

```csharp
        {
            //ExStart:GetFieldNames
            Document doc = new Document();

            string[] fieldNames = doc.MailMerge.GetFieldNames();
            //ExEnd:GetFieldNames
            Console.WriteLine("\nDocument have " + fieldNames.Length + " fields.");
        }

```

## Mapped Data Fields

```csharp
        {
            //ExStart:MappedDataFields
            Document doc = new Document();

            doc.MailMerge.MappedDataFields.Add("MyFieldName_InDocument", "MyFieldName_InDataSource");
            //ExEnd:MappedDataFields
        }

```

## Delete Fields

```csharp
        {
            //ExStart:DeleteFields
            Document doc = new Document();

            doc.MailMerge.DeleteFields();
            //ExEnd:DeleteFields
        }

```

## Field Update Culture

```csharp
        {
            //ExStart:FieldUpdateCultureProvider
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertField(FieldType.FieldTime, true);

            doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
            doc.FieldOptions.FieldUpdateCultureProvider = new FieldUpdateCultureProvider();

            doc.Save(ArtifactsDir + "WorkingWithFields.FieldUpdateCulture.pdf");
            //ExEnd:FieldUpdateCultureProvider
        }

```

## Field Display Results

```csharp
        {
            //ExStart:FieldDisplayResults
            //ExStart:UpdateDocFields
            Document document = new Document(MyDir + "Various fields.docx");

            document.UpdateFields();
            //ExEnd:UpdateDocFields

            foreach (Field field in document.Range.Fields)
                Console.WriteLine(field.DisplayResult);
            //ExEnd:FieldDisplayResults
        }

```

## Evaluate IFCondition

```csharp
        {
            //ExStart:EvaluateIFCondition
            DocumentBuilder builder = new DocumentBuilder();

            FieldIf field = (FieldIf) builder.InsertField("IF 1 = 1", null);
            FieldIfComparisonResult actualResult = field.EvaluateCondition();

            Console.WriteLine(actualResult);
            //ExEnd:EvaluateIFCondition
        }

```

## Convert Fields In Paragraph

```csharp
        {
            //ExStart:ConvertFieldsInParagraph
            Document doc = new Document(MyDir + "Linked fields.docx");

            // Pass the appropriate parameters to convert all IF fields to text that are encountered only in the last 
            // paragraph of the document.
            doc.FirstSection.Body.LastParagraph.Range.Fields.Where(f => f.Type == FieldType.FieldIf).ToList()
                .ForEach(f => f.Unlink());

            doc.Save(ArtifactsDir + "WorkingWithFields.TestFile.docx");
            //ExEnd:ConvertFieldsInParagraph
        }

```

## Convert Fields In Document

```csharp
        {
            //ExStart:ConvertFieldsInDocument
            Document doc = new Document(MyDir + "Linked fields.docx");

            // Pass the appropriate parameters to convert all IF fields encountered in the document (including headers and footers) to text.
            doc.Range.Fields.Where(f => f.Type == FieldType.FieldIf).ToList().ForEach(f => f.Unlink());

            // Save the document with fields transformed to disk
            doc.Save(ArtifactsDir + "WorkingWithFields.ConvertFieldsInDocument.docx");
            //ExEnd:ConvertFieldsInDocument
        }

```

## Convert Fields In Body

```csharp
        {
            //ExStart:ConvertFieldsInBody
            Document doc = new Document(MyDir + "Linked fields.docx");

            // Pass the appropriate parameters to convert PAGE fields encountered to text only in the body of the first section.
            doc.FirstSection.Body.Range.Fields.Where(f => f.Type == FieldType.FieldPage).ToList().ForEach(f => f.Unlink());

            doc.Save(ArtifactsDir + "WorkingWithFields.ConvertFieldsInBody.docx");
            //ExEnd:ConvertFieldsInBody
        }

```

## Change Locale

```csharp
        {
            //ExStart:ChangeLocale
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertField("MERGEFIELD Date");

            // Store the current culture so it can be set back once mail merge is complete.
            CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
            // Set to German language so dates and numbers are formatted using this culture during mail merge.
            Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");

            doc.MailMerge.Execute(new[] { "Date" }, new object[] { DateTime.Now });
            
            Thread.CurrentThread.CurrentCulture = currentCulture;
            
            doc.Save(ArtifactsDir + "WorkingWithFields.ChangeLocale.docx");
            //ExEnd:ChangeLocale
        }

```


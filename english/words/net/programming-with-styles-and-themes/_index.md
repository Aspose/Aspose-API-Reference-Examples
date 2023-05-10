---
title: Programming With Styles And Themes
linktitle: Programming With Styles And Themes
second_title: Aspose.Words for .NET API Reference
description: Tutorials contain access styles, copy styles, get theme properties, set theme properties and insert style separator
type: docs
weight: 1410
url: /words/net/programming-with-styles-and-themes/
---
Tutorials contain access styles, copy styles, get theme properties, set theme properties and insert style separator

## Access Styles

```csharp

            
            Document doc = new Document();

            string styleName = "";

            // Get styles collection from the document.
            StyleCollection styles = doc.Styles;
            foreach (Style style in styles)
            {
                if (styleName == "")
                {
                    styleName = style.Name;
                    Console.WriteLine(styleName);
                }
                else
                {
                    styleName = styleName + ", " + style.Name;
                    Console.WriteLine(styleName);
                }
            }
            
        
```

## Copy Styles

```csharp

            
            Document doc = new Document();
            Document target = new Document(MyDir + "Rendering.docx");

            target.CopyStylesFromTemplate(doc);

            doc.Save(ArtifactsDir + "WorkingWithStylesAndThemes.CopyStyles.docx");
            
        
```

## Get Theme Properties

```csharp

            
            Document doc = new Document();

            Aspose.Words.Themes.Theme theme = doc.Theme;

            Console.WriteLine(theme.MajorFonts.Latin);
            Console.WriteLine(theme.MinorFonts.EastAsian);
            Console.WriteLine(theme.Colors.Accent1);
            
        
```

## Set Theme Properties

```csharp

            
            Document doc = new Document();

            Aspose.Words.Themes.Theme theme = doc.Theme;
            theme.MinorFonts.Latin = "Times New Roman";
            theme.Colors.Hyperlink = Color.Gold;
            
        
```

## Insert Style Separator

```csharp

            
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
            paraStyle.Font.Bold = false;
            paraStyle.Font.Size = 8;
            paraStyle.Font.Name = "Arial";

            // Append text with "Heading 1" style.
            builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
            builder.Write("Heading 1");
            builder.InsertStyleSeparator();

            // Append text with another style.
            builder.ParagraphFormat.StyleName = paraStyle.Name;
            builder.Write("This is text with some other formatting ");

            doc.Save(ArtifactsDir + "WorkingWithStylesAndThemes.InsertStyleSeparator.docx");
            
        
```


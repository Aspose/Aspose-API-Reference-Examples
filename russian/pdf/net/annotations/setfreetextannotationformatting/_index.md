---
title: Установить форматирование произвольного текста аннотаций
linktitle: Установить форматирование произвольного текста аннотаций
second_title: Aspose.PDF для справочника API .NET
description: В этой статье представлено пошаговое руководство о том, как создать аннотацию произвольного текста и указать ее содержимое с помощью Aspose.PDF для .NET.
type: docs
weight: 140
url: /ru/pdf/net/annotations/setfreetextannotationformatting/
---

Aspose.PDF for .NET — это мощный и простой в использовании API для работы с PDF-документами, который позволяет программно работать с PDF-файлами в ваших приложениях .NET. Одной из функций, предоставляемых Aspose.PDF для .NET, является возможность устанавливать произвольное форматирование текстовых аннотаций в документах PDF. В этой статье мы проведем вас через пошаговый процесс настройки форматирования произвольных текстовых аннотаций с помощью Aspose.PDF для .NET.

## Предпосылки

Прежде чем мы начнем, убедитесь, что у вас есть следующие предварительные условия:

- Microsoft Visual Studio 2010 или более поздняя версия
- Aspose.PDF для .NET
- Базовые знания С#



## 1. Создайте новое консольное приложение C#.

Сначала создайте новое консольное приложение C# в Microsoft Visual Studio. Чтобы создать новое консольное приложение, выберите «Файл» > «Создать» > «Проект» > «Visual C#» > «Консольное приложение» в главном меню.

## 2. Добавьте ссылку на Aspose.PDF для .NET.

Затем добавьте ссылку на Aspose.PDF для .NET в свой проект. Для этого щелкните правой кнопкой мыши свой проект на панели «Обозреватель решений», выберите «Добавить» > «Ссылка», а затем перейдите в папку, в которой вы сохранили файл Aspose.PDF для .NET DLL. Выберите файл DLL и нажмите «ОК», чтобы добавить ссылку на ваш проект.

## 3. Настройте среду

После добавления ссылки на Aspose.PDF для .NET необходимо настроить среду. Для этого создайте новую строковую переменную с именем «dataDir» и задайте для нее путь к каталогу, в котором находится ваш PDF-документ. Замените «ВАШ КАТАЛОГ ДОКУМЕНТОВ» в приведенном ниже коде фактическим путем к вашему каталогу документов:

```csharp
// Путь к каталогу документов.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## 4. Откройте PDF-документ

После настройки среды вы можете открыть документ PDF, используя следующий код:

```csharp
// Открыть документ
Document pdfDocument = new Document(dataDir + "SetFreeTextAnnotationFormatting.pdf");
```

Замените «SetFreeTextAnnotationFormatting.pdf» на фактическое имя вашего PDF-документа.

## 5. Настройте внешний вид по умолчанию

Чтобы настроить внешний вид аннотации произвольного текста по умолчанию, необходимо создать экземпляр объекта DefaultAppearance с нужным шрифтом, размером шрифта и цветом. В этом уроке мы устанавливаем шрифт «Arial», размер шрифта 28 и красный цвет.

```csharp
// Создать экземпляр объекта DefaultAppearance
DefaultAppearance default_appearance = new DefaultAppearance("Arial", 28, System.Drawing.Color.Red);
```

## 6. Создайте аннотацию произвольного текста

Теперь, когда вы настроили внешний вид по умолчанию, вы можете создать аннотацию произвольного текста, используя следующий код:

```csharp
// Создать аннотацию
FreeTextAnnotation freetext = new FreeTextAnnotation(pdfDocument.Pages[1], new Aspose.Pdf.Rectangle(200, 400, 400, 600), default_appearance);
```

Приведенный выше код создает новую текстовую аннотацию на второй странице документа PDF. Аннотация будет размещена на (200, 400) и будет иметь ширину 400 и высоту 600.

## 7. Укажите содержание аннотации

После создания аннотации произвольного текста вы можете указать содержимое аннотации, используя следующий код:

```csharp
// Укажите содержимое аннотации
freetext.Contents = "Free Text
```

### Пример исходного кода для установки форматирования аннотаций произвольного текста с использованием Aspose.PDF для .NET
```csharp
  
	// Путь к каталогу документов.
	string dataDir = "YOUR DOCUMENT DIRECTORY";
	
	// Открыть документ
	Document pdfDocument = new Document(dataDir + "SetFreeTextAnnotationFormatting.pdf");

	// Создать экземпляр объекта DefaultAppearance
	DefaultAppearance default_appearance = new DefaultAppearance("Arial", 28, System.Drawing.Color.Red);
	// Создать аннотацию
	FreeTextAnnotation freetext = new FreeTextAnnotation(pdfDocument.Pages[1], new Aspose.Pdf.Rectangle(200, 400, 400, 600), default_appearance);
	// Укажите содержимое аннотации
	freetext.Contents = "Free Text";
	// Добавить аннотацию в коллекцию аннотаций страницы
	pdfDocument.Pages[1].Annotations.Add(freetext);
	dataDir = dataDir + "SetFreeTextAnnotationFormatting_out.pdf";
	// Сохраните обновленный документ
	pdfDocument.Save(dataDir);            

```
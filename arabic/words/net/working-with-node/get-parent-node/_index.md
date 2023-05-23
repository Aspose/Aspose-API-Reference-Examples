---
title: احصل على العقدة الأصلية
linktitle: احصل على العقدة الأصلية
second_title: Aspose.Words لمراجع .NET API
description: تعرف على كيفية الحصول على العقدة الأصلية لعنصر معين باستخدام Aspose.Words for .NET.
type: docs
weight: 10
url: /ar/words/net/working-with-node/get-parent-node/
---

فيما يلي دليل تفصيلي خطوة بخطوة لشرح شفرة المصدر C # أدناه والتي توضح كيفية الحصول على العقدة الأصلية باستخدام Aspose.Words for .NET.

## الخطوة 1: استيراد المراجع الضرورية
قبل أن تبدأ ، تأكد من استيراد المراجع الضرورية لاستخدام Aspose.Words for .NET في مشروعك. يتضمن ذلك استيراد مكتبة Aspose.Words وإضافة مساحات الأسماء المطلوبة إلى ملف المصدر الخاص بك.

```csharp
using Aspose.Words;
using Aspose.Words.Nodes;
```

## الخطوة 2: قم بإنشاء مستند جديد
 في هذه الخطوة ، سننشئ مستندًا جديدًا باستخدام امتداد`Document` فصل.

```csharp
Document doc = new Document();
```

## الخطوة 3: الوصول إلى العقدة الأصلية
للحصول على العقدة الأصلية لعقدة معينة ، نحتاج إلى الوصول إلى تلك العقدة أولاً. في هذا المثال ، نقوم بالوصول إلى أول عقدة فرعية من المستند ، والتي تكون عادةً قسمًا.

```csharp
Node section = doc.FirstChild;
```

## الخطوة 4: تحقق من العقدة الأصلية
الآن بعد أن أصبح لدينا العقدة المحددة ، يمكننا التحقق مما إذا كانت العقدة الأصلية تتطابق مع المستند نفسه. في هذا المثال ، نقارن العقدة الأصلية بالمستند باستخدام عامل المساواة (`==`) وعرض النتيجة.

```csharp
Console.WriteLine("Section parent is the document: " + (doc == section.ParentNode));
```

### عينة من التعليمات البرمجية المصدر للحصول على العقدة الأصلية باستخدام Aspose.Words for .NET


```csharp
	Document doc = new Document();

	// المقطع هو العقدة الفرعية الأولى من المستند.
	Node section = doc.FirstChild;

	// العقدة الرئيسية للقسم هي الوثيقة.
	Console.WriteLine("Section parent is the document: " + (doc == section.ParentNode));
            
```

هذا مثال رمز كامل للحصول على العقدة الأصلية لعقدة معينة باستخدام Aspose.Words for .NET. تأكد من استيراد المراجع الضرورية واتبع الخطوات الموضحة مسبقًا لدمج هذا الرمز في مشروعك.
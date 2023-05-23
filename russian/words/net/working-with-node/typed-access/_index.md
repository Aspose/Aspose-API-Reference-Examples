---
title: Типизированный доступ
linktitle: Типизированный доступ
second_title: Справочник по API Aspose.Words для .NET
description: Узнайте, как использовать типизированный доступ для управления таблицами в Aspose.Words для .NET.
type: docs
weight: 10
url: /ru/words/net/working-with-node/typed-access/
---

Ниже приведено пошаговое руководство по объяснению приведенного ниже исходного кода C#, в котором показано, как использовать функцию типизированного доступа с Aspose.Words для .NET.

## Шаг 1. Импортируйте необходимые ссылки
Прежде чем начать, убедитесь, что вы импортировали в свой проект необходимые ссылки для использования Aspose.Words for .NET. Сюда входит импорт библиотеки Aspose.Words и добавление необходимых пространств имен в исходный файл.

```csharp
using Aspose.Words;
using Aspose.Words.Tables;
```

## Шаг 2: Создайте новый документ
 На этом шаге мы создадим новый документ, используя`Document` сорт.

```csharp
Document doc = new Document();
```

## Шаг 3: Доступ к разделу и телу
Чтобы получить доступ к таблицам, содержащимся в документе, мы должны сначала получить доступ к разделу и телу документа.

```csharp
Section section = doc.FirstSection;
Body body = section.Body;
```

## Шаг 4: Быстрый и типизированный доступ к таблицам
Теперь, когда у нас есть тело документа, мы можем использовать быстрый и типизированный доступ для доступа ко всем таблицам, содержащимся в теле.

```csharp
TableCollection tables = body.Tables;
```

## Шаг 5. Просмотрите таблицы
 Используя`foreach` loop, мы можем пройтись по всем таблицам и выполнить определенные операции над каждой таблицей.

```csharp
foreach(Table table in tables)
{
     // Быстрый и типизированный доступ к первой строке таблицы.
     table.FirstRow?.Remove();

     // Быстрый и типизированный доступ к последней строке таблицы.
     table.LastRow?.Remove();
}
```

В этом примере мы удаляем первую и последнюю строку каждой таблицы, используя быстрый и типизированный доступ, предоставляемый Aspose.Words.

### Пример исходного кода для типизированного доступа с Aspose.Words для .NET

```csharp
	Document doc = new Document();

	Section section = doc.FirstSection;
	Body body = section.Body;
	
	// Быстрый типизированный доступ ко всем дочерним узлам таблицы, содержащимся в теле.
	TableCollection tables = body.Tables;

	foreach (Table table in tables)
	{
		// Быстрый типизированный доступ к первой строке таблицы.
		table.FirstRow?.Remove();

		// Быстрый типизированный доступ к последней строке таблицы.
		table.LastRow?.Remove();
	}
            
```

Это полный пример кода для типизированного доступа к таблицам с помощью Aspose.Words для .NET. Обязательно импортируйте необходимые ссылки и выполните шаги, описанные ранее, чтобы интегрировать этот код в свой проект.

---
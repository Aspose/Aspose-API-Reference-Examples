---
title: Tireleme Geri Çağırma
linktitle: Tireleme Geri Çağırma
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words for .NET'te sözcük hecelemesini işlemek için heceleme geri aramasını nasıl kullanacağınızı öğrenin.
type: docs
weight: 10
url: /tr/words/net/working-with-hyphenation/hyphenation-callback/
---

Bu adım adım öğreticide, size Aspose.Words for .NET'te heceleme geri arama özelliğini nasıl kullanacağınızı göstereceğiz. Sağlanan C# kaynak kodunu açıklayacağız ve bunu kendi projelerinize nasıl uygulayacağınızı göstereceğiz.

Başlamak için geliştirme ortamınızda Aspose.Words for .NET'in kurulu ve yapılandırılmış olduğundan emin olun. Henüz yapmadıysanız, kütüphaneyi resmi siteden indirip yükleyin.

## 1. Adım: Tireleme Hatırlatıcısını Kaydet

 İlk olarak, özel bir kullanarak heceleme geri aramasını kaydedeceğiz.`CustomHyphenationCallback` sınıf. Bu, kelime hecelemesini kendi kurallarımıza göre ele almamıza izin verecektir:

```csharp
Hyphenation.Callback = new CustomHyphenationCallback();
```

 uyguladığınızdan emin olun.`CustomHyphenationCallback`özel ihtiyaçlarınıza göre sınıflandırın.

## 2. Adım: Belgeyi yükleme ve tireleme uygulama

Ardından, belgenizi belirtilen dizinden yükleyin ve Aspose.Words'ü kullanarak kelimeleri tireleyin:

```csharp
string dataDir = "YOUR DOCUMENT DIRECTORY";
Document document = new Document(dataDir + "German text.docx");
document.Save(dataDir + "TreatmentByCesureWithRecall.pdf");
```

## 3. Adım: Eksik Sözlük Hatalarını Ele Alma

Bir heceleme sözlüğünün eksik olması durumunda ilgili istisnayı yakalarız ve bir hata mesajı görüntüleriz:

```csharp
catch (Exception e) when (e.Message.StartsWith("Missing hyphenation dictionary"))
{
     Console.WriteLine(e.Message);
}
```

## 4. Adım: Tireleme Hatırlatıcısını Temizleyin ve Devre Dışı Bırakın

Son olarak, temizlik için ve tireleme hatırlatıcısını kapatmak için aşağıdaki adımları gerçekleştirin:

```csharp
finally
{
     Hyphenation. Callback = null;
}
```

Bu, işlemeyi bitirdikten sonra tireleme hatırlatıcısını temizler ve devre dışı bırakır.

Bu yüzden ! Aspose.Words for .NET'te heceleme geri aramasını başarıyla kullandınız.

### Aspose.Words for .NET ile Tireleme Geri Araması için Örnek Kaynak Kodu

```csharp
try
{
	 // Tireleme geri aramasını kaydedin.
	 Hyphenation.Callback = new CustomHyphenationCallback();
	 string dataDir = "YOUR DOCUMENT DIRECTORY";
	 Document document = new Document(dataDir + "German text.docx");
	 document.Save(dataDir + "TreatmentByCesureWithRecall.pdf");
}
catch (Exception e) when (e.Message.StartsWith("Missing hyphenation dictionary"))
{
	 Console.WriteLine(e.Message);
}
finally
{
	 Hyphenation. Callback = null;
}

```

Bu kodu kendi projelerinizde kullanmaktan ve özel ihtiyaçlarınıza uyacak şekilde değiştirmekten çekinmeyin.
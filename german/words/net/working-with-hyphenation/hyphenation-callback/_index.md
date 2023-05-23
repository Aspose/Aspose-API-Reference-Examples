---
title: Rückruf zur Silbentrennung
linktitle: Rückruf zur Silbentrennung
second_title: Aspose.Words für .NET API-Referenz
description: Erfahren Sie, wie Sie den Silbentrennungsrückruf in Aspose.Words für .NET verwenden, um die Silbentrennung von Wörtern zu verarbeiten.
type: docs
weight: 10
url: /de/words/net/working-with-hyphenation/hyphenation-callback/
---

In dieser Schritt-für-Schritt-Anleitung zeigen wir Ihnen, wie Sie die Silbentrennungs-Rückruffunktion in Aspose.Words für .NET verwenden. Wir erklären Ihnen den bereitgestellten C#-Quellcode und zeigen Ihnen, wie Sie ihn in Ihren eigenen Projekten implementieren.

Stellen Sie zunächst sicher, dass Aspose.Words für .NET in Ihrer Entwicklungsumgebung installiert und konfiguriert ist. Wenn Sie es noch nicht getan haben, laden Sie die Bibliothek von der offiziellen Website herunter und installieren Sie sie.

## Schritt 1: Silbentrennungserinnerung speichern

 Zuerst registrieren wir den Silbentrennungsrückruf mithilfe einer benutzerdefinierten Funktion`CustomHyphenationCallback` Klasse. Dadurch können wir die Silbentrennung von Wörtern nach unseren eigenen Regeln handhaben:

```csharp
Hyphenation.Callback = new CustomHyphenationCallback();
```

 Stellen Sie sicher, dass Sie das implementiert haben`CustomHyphenationCallback`Unterricht nach Ihren spezifischen Bedürfnissen.

## Schritt 2: Laden des Dokuments und Anwenden der Silbentrennung

Laden Sie als Nächstes Ihr Dokument aus dem angegebenen Verzeichnis und trennen Sie die Wörter mit Aspose.Words:

```csharp
string dataDir = "YOUR DOCUMENT DIRECTORY";
Document document = new Document(dataDir + "German text.docx");
document.Save(dataDir + "TreatmentByCesureWithRecall.pdf");
```

## Schritt 3: Behandeln von fehlenden Wörterbuchfehlern

Falls ein Silbentrennungswörterbuch fehlt, fangen wir die entsprechende Ausnahme ab und zeigen eine Fehlermeldung an:

```csharp
catch (Exception e) when (e.Message.StartsWith("Missing hyphenation dictionary"))
{
     Console.WriteLine(e.Message);
}
```

## Schritt 4: Silbentrennungserinnerung bereinigen und deaktivieren

Führen Sie abschließend aus Gründen der Sauberkeit und zum Deaktivieren der Silbentrennungserinnerung die folgenden Schritte aus:

```csharp
finally
{
     Hyphenation. Callback = null;
}
```

Dadurch wird die Silbentrennungserinnerung nach Abschluss der Verarbeitung bereinigt und deaktiviert.

So ! Sie haben den Silbentrennungs-Callback in Aspose.Words für .NET erfolgreich verwendet.

### Beispielquellcode für Silbentrennungsrückruf mit Aspose.Words für .NET

```csharp
try
{
	 // Rückruf für Silbentrennung registrieren.
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

Sie können diesen Code gerne in Ihren eigenen Projekten verwenden und an Ihre spezifischen Bedürfnisse anpassen.
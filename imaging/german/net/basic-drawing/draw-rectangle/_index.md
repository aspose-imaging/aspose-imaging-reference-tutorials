---
date: 2026-02-12
description: Erfahren Sie, wie Sie ein leeres Bild mit Aspose erstellen und ein Rechteck
  in .NET mit Aspose.Imaging zeichnen – ein kurzer Leitfaden zur Bildbearbeitung in
  Ihren .NET‑Anwendungen.
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Leeres Bild erstellen mit Aspose – Rechtecke in .NET zeichnen
url: /de/net/basic-drawing/draw-rectangle/
weight: 14
---

.

Let's craft.

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Blank Image Aspose erstellen – Rechtecke in .NET zeichnen

Das Erstellen und Bearbeiten von Bildern in .NET‑Anwendungen kann einschüchternd wirken, aber mit Aspose.Imaging können Sie **blank image Aspose** in nur wenigen Codezeilen erzeugen und anschließend Formen darauf zeichnen. In diesem Tutorial führen wir Sie durch den gesamten Prozess — vom Einrichten einer leeren Leinwand bis zum Zeichnen von Rechtecken—damit Sie sofort Grafiken zu Ihren .NET‑Projekten hinzufügen können.

## Schnellantworten
- **Was bedeutet „create blank image Aspose“?** Es bedeutet, ein leeres Bitmap mithilfe der Aspose.Imaging‑API zu erzeugen.  
- **Wie zeichnet man ein Rechteck in .NET mit Aspose?** Verwenden Sie die Methode `Graphics.DrawRectangle`, nachdem Sie ein `Graphics`‑Objekt initialisiert haben.  
- **Welches NuGet‑Paket wird benötigt?** `Aspose.Imaging` (neueste Version).  
- **Kann ich das Bild als PNG, JPEG oder BMP speichern?** Ja – ändern Sie einfach die Bildoptionen (z. B. `BmpOptions`, `JpegOptions`).  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion reicht für die Evaluierung; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.

## Was bedeutet „create blank image Aspose“?
Ein leeres Bild zu erstellen bedeutet, einen Pixelpuffer mit definierter Breite, Höhe und Pixelformat zu reservieren. Aspose.Imaging übernimmt die Low‑Level‑Details und liefert Ihnen eine sofort nutzbare Zeichenfläche, ohne dass Sie sich mit GDI+ oder System.Drawing befassen müssen.

## Warum Aspose.Imaging zum Zeichnen von Rechtecken in .NET verwenden?
- **Cross‑platform** – funktioniert unter Windows, Linux und macOS.  
- **Keine nativen Abhängigkeiten** – reiner Managed‑Code, ideal für Server‑Umgebungen.  
- **Umfangreiche Zeichen‑API** – unterstützt Pens, Brushes, Anti‑Aliasing und viele Formtypen.  
- **Hohe Performance** – optimiert für große Bilder und Batch‑Verarbeitung.

## Voraussetzungen

1. **Aspose.Imaging für .NET** – laden Sie es von der [download page](https://releases.aspose.com/imaging/net/) herunter.  
2. **Entwicklungsumgebung** – Visual Studio, VS Code oder jede .NET‑kompatible IDE.  
3. **.NET‑Runtime** – .NET 6+ oder .NET Framework 4.7.2+.  

Jetzt, wo alles eingerichtet ist, tauchen wir in den Code ein.

## Wie erstellt man ein blank image Aspose in .NET?

### Schritt 1: Die erforderlichen Namespaces importieren

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

Diese Namespaces geben Ihnen Zugriff auf die Kern‑Imaging‑Klassen, Brush‑Typen und Bild‑Speicheroptionen.

### Schritt 2: Ein blank image (die Leinwand) erstellen

```csharp
string dataDir = "Your Document Directory";  // Set the path to your document directory
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Your drawing code will go here
        image.Save();
    }
}
```

In diesem Block:

* Definieren wir den Ausgabepfad (`dataDir`).  
* Konfigurieren `BmpOptions` für ein 32‑Bit‑Pixelformat.  
* Erzeugen ein **blank image** mit 100 × 100 Pixeln.  

### Schritt 3: Wie zeichnet man ein rectangle .net mit Aspose.Imaging

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` füllt die Leinwand mit einer Hintergrundfarbe (gelb in diesem Beispiel).  
* `DrawRectangle` zeichnet zwei Rechtecke – eines mit einem einfachen roten Pen, ein weiteres mit einem blauen Solid‑Brush – zum visuellen Kontrast.

### Schritt 4: Das Bild speichern

```csharp
image.Save();
```

Der Aufruf von `Save` schreibt das Bitmap mithilfe der zuvor definierten Optionen in das Dateisystem.

## Häufige Probleme & Tipps

| Problem | Ursache | Lösung |
|---------|----------|--------|
| **Blank image erscheint schwarz** | Hintergrund nicht gelöscht | Rufen Sie `graphic.Clear(Color.YourColor)` vor dem Zeichnen auf. |
| **File not found‑Exception** | `dataDir` verweist auf einen nicht existierenden Ordner | Stellen Sie sicher, dass das Verzeichnis existiert, oder verwenden Sie `Path.Combine` mit `Environment.CurrentDirectory`. |
| **Falsche Farben** | Verwendung von `System.Drawing.Color` statt `Aspose.Imaging.Color` | Immer `Aspose.Imaging.Color` importieren. |
| **Performance‑Einbrüche bei großen Bildern** | Standard‑`BmpOptions` mit hoher Bits‑per‑Pixel‑Zahl | Zu `JpegOptions` oder `PngOptions` für Kompression wechseln. |

## Häufig gestellte Fragen (Erweitert)

**F: Kann ich neben Rechtecken auch andere Formen zeichnen?**  
A: Auf jeden Fall. Aspose.Imaging bietet Methoden wie `DrawEllipse`, `DrawLine` und `DrawPolygon`.

**F: Ist die Bibliothek für den kommerziellen Einsatz kostenlos?**  
A: Nein, Aspose.Imaging ist ein kommerzielles Produkt, Sie können es jedoch mit einer kostenlosen Testversion evaluieren, die [hier](https://releases.aspose.com/) verfügbar ist.

**F: Funktioniert das sowohl unter Windows als auch in Web‑Anwendungen?**  
A: Ja, derselbe Code läuft in ASP.NET, Blazor und Konsolen‑Apps.

**F: Wie ändere ich das Ausgabeformat zu PNG?**  
A: Ersetzen Sie `BmpOptions` durch `PngOptions` und passen Sie die Dateierweiterung entsprechend an.

**F: Wo finde ich ausführlichere Dokumentation?**  
A: Greifen Sie auf die vollständige API‑Referenz [hier](https://reference.aspose.com/imaging/net/) zu und besuchen Sie die Community im [Aspose.Imaging‑Forum](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Zuletzt aktualisiert:** 2026-02-12  
**Getestet mit:** Aspose.Imaging 24.12 für .NET  
**Autor:** Aspose
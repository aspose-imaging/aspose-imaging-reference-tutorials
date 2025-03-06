---
title: Zeichnen von Ellipsen in Aspose.Imaging für .NET
linktitle: Zeichnen Sie eine Ellipse in Aspose.Imaging für .NET
second_title: Aspose.Imaging .NET-Bildverarbeitungs-API
description: Lernen Sie, Ellipsen in Aspose.Imaging für .NET zu zeichnen, einer vielseitigen Bildbearbeitungsbibliothek. Erstellen Sie ganz einfach atemberaubende Grafiken.
weight: 12
url: /de/net/basic-drawing/draw-ellipse/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zeichnen von Ellipsen in Aspose.Imaging für .NET

In diesem Tutorial führen wir Sie durch den Prozess des Zeichnens von Ellipsen mit Aspose.Imaging für .NET. Aspose.Imaging ist eine leistungsstarke Bibliothek, mit der Sie Bilder in verschiedenen Formaten in Ihren .NET-Anwendungen bearbeiten und erstellen können. Wir beginnen mit der Einführung des Konzepts und der Voraussetzungen und unterteilen dann jedes Beispiel in mehrere Schritte, um ein klares Verständnis zu gewährleisten.

## Voraussetzungen

Bevor wir uns mit dem Zeichnen von Ellipsen in Aspose.Imaging für .NET befassen, sollten Sie sicherstellen, dass die folgenden Voraussetzungen erfüllt sind:

1. Visual Studio: Stellen Sie sicher, dass Visual Studio für die .NET-Entwicklung auf Ihrem System installiert ist.

2.  Aspose.Imaging für .NET: Sie müssen Aspose.Imaging für .NET installiert haben. Wenn nicht, können Sie es hier herunterladen[Download-Seite](https://releases.aspose.com/imaging/net/).

3. Ihr Dokumentenverzeichnis: Erstellen Sie ein Verzeichnis, in dem Sie die während dieses Tutorials erstellten Bilder speichern.

Nachdem wir nun die Voraussetzungen geschaffen haben, können wir beginnen.

## Namespaces importieren

In diesem Schritt importieren wir die notwendigen Namespaces, um mit Aspose.Imaging zu arbeiten. Folgen Sie den unteren Schritten:

### Schritt 1: Öffnen Sie Ihr Visual Studio-Projekt

Starten Sie Visual Studio und öffnen Sie Ihr .NET-Projekt dort, wo Sie Aspose.Imaging verwenden möchten.

### Schritt 2: Using-Anweisungen hinzufügen

Fügen Sie in Ihrer Codedatei die folgenden using-Anweisungen hinzu, um die erforderlichen Namespaces einzuschließen:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.Colors;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.FileFormats.Bmp.Options;
using Aspose.Imaging.Sources;
```

Nachdem Sie nun die erforderlichen Namespaces importiert haben, können Sie eine Ellipse zeichnen.

## Ellipse zeichnen

Wir stellen Ihnen nun eine Schritt-für-Schritt-Anleitung zum Zeichnen einer Ellipse mit Aspose.Imaging für .NET zur Verfügung. Dieses Beispiel führt Sie durch den Prozess.

### Schritt 1: Richten Sie die Ausgabedatei ein

Bevor Sie eine Ellipse zeichnen, müssen Sie die Ausgabedatei einrichten. So können Sie es machen:

```csharp
string dataDir = "Your Document Directory";
using (FileStream stream = new FileStream(dataDir + "DrawingEllipse_out.bmp", FileMode.Create))
{
```

In diesem Codeausschnitt erstellen wir einen FileStream, um den Pfad der Ausgabedatei anzugeben.

### Schritt 2: BmpOptions konfigurieren

Verwenden Sie den folgenden Code, um das BMP-Format und andere Eigenschaften zu konfigurieren:

```csharp
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
saveOptions.Source = new StreamSource(stream);
```

Hier erstellen wir eine BmpOptions-Instanz, legen die Bittiefe fest und geben den Quellstream an.

### Schritt 3: Erstellen Sie ein Bild

 Erstellen Sie eine Instanz von`Image` Klasse mit den angegebenen Optionen und Dimensionen:

```csharp
using (Image image = Image.Create(saveOptions, 100, 100))
{
```

In diesem Schritt erstellen wir ein Bild mit einer Größe von 100x100 Pixeln.

### Schritt 4: Grafiken initialisieren und Oberfläche löschen

Initialisieren Sie eine Grafikinstanz und löschen Sie die Bildoberfläche:

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
```

Dieser Code erstellt ein Grafikobjekt und löscht das Bild mit einem gelben Hintergrund.

### Schritt 5: Ellipsen zeichnen

Zeichnen wir nun Ellipsen auf das Bild:

```csharp
graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

Hier zeichnen wir eine rot gepunktete Ellipse und eine blaue durchgezogene Ellipse auf das Bild.

### Schritt 6: Speichern Sie das Bild

Speichern Sie abschließend das Bild:

```csharp
image.Save();
```

## Abschluss

Das Zeichnen von Ellipsen in Aspose.Imaging für .NET ist ein unkomplizierter Vorgang. Mit den in diesem Tutorial beschriebenen Schritten können Sie ganz einfach Bilder in Ihren .NET-Anwendungen erstellen und bearbeiten. Aspose.Imaging bietet eine breite Palette an Bildbearbeitungsfunktionen und ist damit ein wertvolles Werkzeug für Entwickler.

## FAQs

### F1: Was sind die Hauptfunktionen von Aspose.Imaging für .NET?

Aspose.Imaging für .NET bietet eine breite Palette von Funktionen, einschließlich Bilderstellung, -bearbeitung, -konvertierung und -rendering. Es unterstützt verschiedene Bildformate und bietet erweiterte Bildbearbeitungsfunktionen.

### F2: Kann ich Aspose.Imaging für .NET sowohl in Windows- als auch in Webanwendungen verwenden?

Ja, Sie können Aspose.Imaging für .NET sowohl in Windows-Desktop- als auch in Webanwendungen verwenden, wodurch es für verschiedene Entwicklungsszenarien vielseitig einsetzbar ist.

### F3: Gibt es eine kostenlose Testversion für Aspose.Imaging für .NET?

 Ja, Sie können eine kostenlose Testversion von Aspose.Imaging für .NET erhalten[Testseite](https://releases.aspose.com/).

### F4: Wo finde ich eine umfassende Dokumentation für Aspose.Imaging für .NET?

 Eine ausführliche Dokumentation zu Aspose.Imaging für .NET finden Sie unter[Dokumentationsseite](https://reference.aspose.com/imaging/net/).

### F5: Wie kann ich Unterstützung für Aspose.Imaging für .NET erhalten, wenn Probleme auftreten?

 Sie können Unterstützung suchen und sich mit der Aspose-Community austauschen[Forum](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

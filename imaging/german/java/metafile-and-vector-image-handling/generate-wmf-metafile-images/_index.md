---
title: Erstellen von WMF-Bildern mit Aspose.Imaging für Java
linktitle: Generieren Sie WMF-Metadateibilder
second_title: Aspose.Imaging Java-Bildverarbeitungs-API
description: Erfahren Sie, wie Sie mit Aspose.Imaging WMF-Metadateibilder in Java erstellen. Befolgen Sie diese Schritt-für-Schritt-Anleitung für leistungsstarke Funktionen zur Bildgenerierung.
type: docs
weight: 10
url: /de/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/
---
Möchten Sie WMF-Bilder (Windows Metafile) mit Ihren Java-Anwendungen erstellen? Aspose.Imaging für Java ist ein leistungsstarkes Tool, mit dem Sie problemlos WMF-Bilder generieren können. In dieser Schritt-für-Schritt-Anleitung führen wir Sie durch den Prozess der Verwendung von Aspose.Imaging für Java zum Erstellen von WMF-Metadateibildern. 

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Eine auf Ihrem Computer eingerichtete Java-Entwicklungsumgebung.
-  Aspose.Imaging für Java-Bibliothek installiert. Sie können es hier herunterladen[Webseite](https://releases.aspose.com/imaging/java/).
- Grundkenntnisse der Java-Programmierung.

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete für Ihre Java-Anwendung, um Aspose.Imaging für Java zu verwenden:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.color.*;
import com.aspose.imaging.coreexceptions.ImageLoadException;
import com.aspose.imaging.imageoptions.WmfOptions;
import com.aspose.imaging.internal.system.drawing.*;
import com.aspose.imaging.internal.system.drawing.imaging.*;
import com.aspose.imaging.pen.*;
import com.aspose.imaging.system.drawing.*;
```

## Schritt 1: Erstellen Sie eine Leinwand

 Um mit der Erstellung Ihres WMF-Bildes zu beginnen, müssen Sie eine Leinwand erstellen, auf der Sie Formen zeichnen können. Der`WmfRecorderGraphics2D` Die Klasse stellt Ihnen diese Leinwand zur Verfügung. So können Sie eine Instanz davon erstellen:

```java
// Der Pfad zum Dokumentenverzeichnis.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

Im obigen Code geben wir die Leinwandabmessungen (100x100) und die Auflösung (96 DPI) an.

## Schritt 2: Hintergrundfarbe festlegen

 Als nächstes definieren Sie die Hintergrundfarbe für Ihre Leinwand. Du kannst den ... benutzen`setBackgroundColor` Methode zum Festlegen der Hintergrundfarbe:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

In diesem Beispiel stellen wir die Hintergrundfarbe auf weißen Rauch ein.

## Schritt 3: Definieren Sie Stift und Pinsel

Um Formen auf der Leinwand zu zeichnen, müssen Sie einen Stift und einen Pinsel definieren. Der Stift dient zum Zeichnen von Umrissen und der Pinsel zum Füllen von Formen. So können Sie einen Stift und einen festen Pinsel erstellen:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

In diesem Code erstellen wir einen blauen Stift und einen gelbgrünen Vollpinsel.

## Schritt 4: Formen füllen und zeichnen

Füllen und zeichnen wir nun einige Grundformen auf der Leinwand. Wir beginnen mit einem Polygon:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Hier füllen und zeichnen wir ein Polygon mit dem angegebenen Stift und Pinsel. Sie können die Koordinaten und Formen nach Bedarf anpassen.

## Schritt 5: Verwenden Sie HatchBrush

 Um Ihren Formen Texturen hinzuzufügen, können Sie a verwenden`HatchBrush`. Zum Beispiel:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

In diesem Code erstellen wir einen Kreuzschraffurpinsel mit den Farben Weiß und Silber.

## Schritt 6: Ellipse füllen und zeichnen

Füllen wir die Leinwand aus und zeichnen wir eine Ellipse:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

Sie können die Position und Größe der Ellipse nach Bedarf anpassen.

## Schritt 7: Zeichnen Sie einen Bogen und einen kubischen Bezier

Auch das Zeichnen komplexerer Formen ist möglich. So zeichnen Sie einen Bogen und eine kubische Bezier-Kurve:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

Im obigen Code zeichnen wir zunächst einen Bogen im gepunkteten Linienstil und dann eine kubische Bezier-Kurve mit einem durchgehend roten Stift.

## Schritt 8: Bilder hinzufügen

Sie können Ihrer WMF-Metadatei auch Bilder hinzufügen. So geht's:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

In diesem Schritt laden wir ein Bild und platzieren es an den angegebenen Koordinaten (50, 50) auf der Leinwand.

## Schritt 9: Linien und Kreis zeichnen

Um Linien und Kreisformen hinzuzufügen, können Sie diesen Beispielen folgen:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Hier zeichnen wir eine Linie und füllen/zeichnen eine Kreisform mit dem angegebenen Stift und Pinsel.

## Schritt 10: Zeichnen Sie Polylinie und Text

Das Hinzufügen von Text und Polylinien ist unkompliziert:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

Sie können Schriftart, Text und Polylinienpunkte nach Bedarf anpassen.

## Schritt 11: Speichern Sie das WMF-Bild

Sobald Sie Ihr WMF-Image erstellt haben, ist es an der Zeit, es zu speichern:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Dieser Code speichert das WMF-Bild im angegebenen Verzeichnis.

Das ist es! Sie haben mit Aspose.Imaging für Java erfolgreich ein WMF-Metadateibild generiert.

## Abschluss

In diesem Tutorial haben wir untersucht, wie Sie WMF-Metadateibilder mit Aspose.Imaging für Java erstellen. Wir haben die notwendigen Voraussetzungen abgedeckt, Pakete importiert und Schritt-für-Schritt-Anleitungen zum Zeichnen verschiedener Formen, zum Hinzufügen von Texturen, zum Einfügen von Bildern und zum Speichern des endgültigen Bilds bereitgestellt. Aspose.Imaging für Java bietet leistungsstarke Tools zur Bildbearbeitung und -erstellung und ist damit eine wertvolle Ressource für Ihre Java-Anwendungen.

## FAQs

### F1: Was ist ein WMF-Bildformat?

A1: WMF steht für Windows Metafile, ein Vektorgrafikformat, das zum Speichern von Bildern, Zeichnungen und anderen grafischen Daten verwendet wird. Es wird häufig in Windows-Anwendungen verwendet und kann ohne Qualitätsverlust einfach skaliert werden.

### F2: Wo kann ich Aspose.Imaging für Java herunterladen?

 A2: Sie können Aspose.Imaging für Java von herunterladen[Webseite](https://releases.aspose.com/imaging/java/).

### F3: Benötige ich fortgeschrittene Programmierkenntnisse, um Aspose.Imaging für Java zu verwenden?

A3: Während grundlegende Java-Programmierkenntnisse erforderlich sind, bietet Aspose.Imaging für Java eine benutzerfreundliche API, die Bildbearbeitungs- und Erstellungsaufgaben vereinfacht.

### F4: Kann ich Aspose.Imaging für Java für kommerzielle Zwecke verwenden?

 A4: Ja, Aspose.Imaging für Java bietet kommerzielle Lizenzen für Unternehmen und Entwickler an. Sie können eine Lizenz erwerben bei[Hier](https://purchase.aspose.com/buy).

### F5: Wo kann ich Unterstützung erhalten oder Fragen zu Aspose.Imaging für Java stellen?

 A5: Sie können Unterstützung finden und sich mit der Aspose-Community austauschen[Aspose.Imaging-Foren](https://forum.aspose.com/).
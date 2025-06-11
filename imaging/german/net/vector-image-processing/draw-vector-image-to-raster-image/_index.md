---
"description": "Erfahren Sie, wie Sie mit Aspose.Imaging Vektorbilder in .NET in Rasterbilder konvertieren. Eine Schritt-für-Schritt-Anleitung für effiziente Bildverarbeitung."
"linktitle": "Zeichnen Sie ein Vektorbild in ein Rasterbild in Aspose.Imaging für .NET"
"second_title": "Aspose.Imaging .NET Bildverarbeitungs-API"
"title": "Zeichnen Sie ein Vektorbild in ein Rasterbild in Aspose.Imaging für .NET"
"url": "/de/net/vector-image-processing/draw-vector-image-to-raster-image/"
"weight": 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Zeichnen Sie ein Vektorbild in ein Rasterbild in Aspose.Imaging für .NET


Möchten Sie Vektorbilder in Ihren .NET-Anwendungen mühelos in Rasterbilder konvertieren? Aspose.Imaging für .NET bietet hierfür eine effiziente Lösung. In dieser Schritt-für-Schritt-Anleitung führen wir Sie durch den Prozess der Konvertierung von Vektorbildern in Rasterbilder mit Aspose.Imaging für .NET. 

## Voraussetzungen

Bevor wir mit dem Tutorial beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

### 1. Aspose.Imaging für .NET

Sie sollten Aspose.Imaging für .NET installiert haben. Falls nicht, können Sie es von der Website herunterladen unter [Laden Sie Aspose.Imaging für .NET herunter](https://releases.aspose.com/imaging/net/).

### 2. .NET-Entwicklungsumgebung

Stellen Sie sicher, dass auf Ihrem Computer eine .NET-Entwicklungsumgebung eingerichtet ist. Sie können Visual Studio oder ein anderes .NET-Entwicklungstool verwenden.

Lassen Sie uns nun den Vorgang des Zeichnens von Vektorbildern in Rasterbilder in einfache, leicht verständliche Schritte unterteilen:

## Schritt 1: Initialisieren Sie Ihr Projekt

Erstellen Sie zunächst ein neues .NET-Projekt in Ihrer Entwicklungsumgebung. Stellen Sie sicher, dass Aspose.Imaging für .NET in Ihr Projekt integriert ist.

## Schritt 2: Laden Sie das Vektorbild

In diesem Schritt laden wir das Vektorbild (im SVG-Format), das Sie in ein Rasterbild umwandeln möchten.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## Schritt 3: Rastern Sie das Vektorbild

Jetzt müssen wir das SVG-Bild in das PNG-Format rastern. Hier erfolgt die Konvertierung vom Vektor zum Raster.

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## Schritt 4: Laden Sie das Rasterbild

Laden Sie nach der Rasterung das PNG-Bild aus dem Stream zum weiteren Zeichnen.

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## Schritt 5: Zeichnen Sie das Rasterbild

Jetzt können wir das Rasterbild auf das vorhandene SVG-Bild zeichnen.

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## Schritt 6: Speichern Sie das Ergebnis

Speichern Sie abschließend das Ergebnisbild. Sie haben nun ein Rasterbild, das Ihr Vektorbild enthält.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## Abschluss

In diesem Tutorial haben wir gezeigt, wie Sie mit Aspose.Imaging für .NET Vektorbilder in Rasterbilder konvertieren. Mit diesen einfachen Schritten können Sie diese Funktionalität mühelos in Ihre .NET-Anwendungen integrieren.

### Häufig gestellte Fragen

### Was ist Aspose.Imaging für .NET?
Aspose.Imaging für .NET ist eine .NET-Bibliothek, die leistungsstarke Bildverarbeitungsfunktionen bietet, einschließlich der Möglichkeit, mit verschiedenen Bildformaten zu arbeiten, Bilder zu konvertieren und erweiterte Bildbearbeitungsaufgaben durchzuführen.

### Wo finde ich die Dokumentation für Aspose.Imaging für .NET?
Die Dokumentation für Aspose.Imaging für .NET finden Sie [Hier](https://reference.aspose.com/imaging/net/).

### Gibt es eine kostenlose Testversion?
Ja, Sie können auf eine kostenlose Testversion von Aspose.Imaging für .NET zugreifen [Hier](https://releases.aspose.com/).

### Wie erhalte ich eine temporäre Lizenz für Aspose.Imaging für .NET?
Wenn Sie eine vorübergehende Lizenz benötigen, können Sie diese erhalten [Hier](https://purchase.aspose.com/temporary-license/).

### Wo erhalte ich Support für Aspose.Imaging für .NET?
Für Support oder Fragen besuchen Sie bitte die [Aspose.Imaging-Forum](https://forum.aspose.com/).


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
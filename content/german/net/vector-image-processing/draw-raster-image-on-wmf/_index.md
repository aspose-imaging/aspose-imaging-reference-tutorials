---
title: Zeichnen Sie ein Rasterbild auf WMF in Aspose.Imaging für .NET
linktitle: Zeichnen Sie ein Rasterbild auf WMF in Aspose.Imaging für .NET
second_title: Aspose.Imaging .NET-Bildverarbeitungs-API
description: Erfahren Sie, wie Sie mit Aspose.Imaging Rasterbilder in WMF-Dokumenten in .NET zeichnen. Werten Sie Ihre .NET-Projekte mit kreativen Bildüberlagerungen auf.
type: docs
weight: 12
url: /de/net/vector-image-processing/draw-raster-image-on-wmf/
---

Im Bereich der .NET-Entwicklung gilt Aspose.Imaging als vielseitiges Tool, das Entwicklern die Bearbeitung und Arbeit mit Bildern in verschiedenen Formaten ermöglicht. Aspose.Imaging bietet unter anderem die Funktion zum Zeichnen von Rasterbildern in Windows Metafile (WMF)-Dokumenten. Diese Funktionalität ist äußerst wertvoll, wenn Sie Bilder auf vektorbasierten Dokumenten überlagern müssen und eröffnet Ihnen eine Welt voller kreativer Möglichkeiten.

## Voraussetzungen

Bevor Sie mit Aspose.Imaging für .NET in die Welt des Zeichnens von Rasterbildern auf WMF-Dokumenten eintauchen, müssen Sie einige Voraussetzungen erfüllen:

### 1. Aspose.Imaging für .NET-Bibliothek

 Stellen Sie zunächst sicher, dass die Aspose.Imaging for .NET-Bibliothek in Ihr .NET-Projekt integriert ist. Sie können diese Bibliothek erhalten unter[Laden Sie es von Aspose.Releases herunter](https://releases.aspose.com/imaging/net/).

### 2. Grundlegendes Verständnis von .NET

Sie sollten über grundlegende Kenntnisse der .NET-Entwicklung verfügen, einschließlich der Erstellung und Verwaltung von Projekten, der Arbeit mit Bibliotheken und dem Schreiben von Code in C#.

### 3. Bilddateien

Bereiten Sie die Bilddateien vor, die Sie in das WMF-Dokument zeichnen möchten. Sie sollten über die Quellbilddatei in einem Rasterformat (z. B. PNG) und ein vorhandenes WMF-Dokument verfügen, das als Leinwand dient.

Wenn diese Voraussetzungen erfüllt sind, sehen wir uns die Schritt-für-Schritt-Anleitung zum Zeichnen eines Rasterbilds in einem WMF-Dokument mit Aspose.Imaging für .NET an.

## Namespaces importieren

Bevor Sie beginnen, stellen Sie sicher, dass Sie die erforderlichen Namespaces in Ihren C#-Code importieren:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Examples.CSharp;
using Aspose.Imaging.FileFormats.Wmf;
using Aspose.Imaging.FileFormats.Png;
using Aspose.Imaging.FileFormats.Wmf.Graphics;
using Aspose.Imaging.FileFormats.Wmf.Objects;
```

## Schritt 1: Bilddateien laden

Zunächst müssen Sie das Quellbild und das WMF-Dokument in Ihr Projekt laden. Der folgende Code zeigt, wie diese Dateien geladen werden:

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "Your Document Directory";

// Laden Sie das zu zeichnende Bild
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
{
    // Laden Sie das WMF-Bild zum Zeichnen darauf (Zeichenoberfläche)
    using (WmfImage canvasImage = (WmfImage)Image.Load(dataDir + "asposenet_222_wmf_200.wmf"))
    {
        // Fahren Sie mit dem nächsten Schritt fort.
    }
}
```

## Schritt 2: Grafiken initialisieren

Um das Rasterbild auf das WMF-Dokument zu zeichnen, müssen Sie die Grafiken initialisieren. So können Sie es machen:

```csharp
WmfRecorderGraphics2D graphics = WmfRecorderGraphics2D.FromWmfImage(canvasImage);
```

## Schritt 3: Zeichnen Sie das Bild

Jetzt können Sie das Rasterbild auf das WMF-Dokument zeichnen. Geben Sie die Position und Größe des Bildes innerhalb der Leinwand sowie die Abmessungen des Quellbildes an. Das gezeichnete Bild wird gestreckt, wenn die Quell- und Zielgrößen unterschiedlich sind:

```csharp
graphics.DrawImage(
    imageToDraw,
    new Rectangle(67, 67, canvasImage.Width, canvasImage.Height),
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    GraphicsUnit.Pixel);
```

## Schritt 4: Speichern Sie das Ergebnis

Wenn Sie den Zeichenvorgang abgeschlossen haben, speichern Sie das Ergebnis als neues WMF-Dokument:

```csharp
using (WmfImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_222_wmf_200.DrawImage.wmf");
}
```

## Abschluss

In dieser Schritt-für-Schritt-Anleitung haben wir untersucht, wie Sie mit Aspose.Imaging für .NET ein Rasterbild in ein WMF-Dokument zeichnen. Mit dieser Funktionalität können Sie Vektor- und Rasterbilder kombinieren, was endlose Möglichkeiten für kreative Projekte eröffnet.

Denken Sie daran, die Aspose.Imaging for .NET-Bibliothek von der Website zu beziehen und sicherzustellen, dass Sie über die erforderlichen Bilddateien für Ihr Projekt verfügen. Mit diesen Schritten und den bereitgestellten Codeausschnitten können Sie Bildzeichnungen nahtlos in Ihre .NET-Anwendungen integrieren.

### Häufig gestellte Fragen

### Kann ich Aspose.Imaging für .NET mit anderen .NET-Bibliotheken und Frameworks verwenden?
   - Ja, Aspose.Imaging für .NET ist mit verschiedenen .NET-Bibliotheken und Frameworks kompatibel und eignet sich daher vielseitig für die Integration in verschiedene Projekte.

### Gibt es Einschränkungen beim Zeichnen von Rasterbildern in WMF-Dokumenten?
   - Während Aspose.Imaging für .NET leistungsstarke Bildbearbeitungsfunktionen bietet, ist es wichtig, die Größe und Auflösung des Dokuments zu berücksichtigen, um optimale Ergebnisse zu gewährleisten.

### Kann ich mehrere Bilder in ein einzelnes WMF-Dokument zeichnen?
   - Ja, Sie können mehrere Rasterbilder in ein WMF-Dokument zeichnen, indem Sie die Zeichenschritte für jedes Bild wiederholen.

### Wie kann ich mit Aspose.Imaging für .NET Text oder Formen zu einem WMF-Dokument hinzufügen?
   - Aspose.Imaging für .NET bietet zahlreiche Funktionen zum Hinzufügen von Text und Formen zu WMF-Dokumenten. Ausführliche Beispiele finden Sie in der Dokumentation.

### Wo finde ich Unterstützung und zusätzliche Ressourcen für Aspose.Imaging für .NET?
   -  Eine ausführliche Dokumentation und Hilfe von der Aspose.Imaging-Community finden Sie unter[Aspose.Imaging-Supportforum](https://forum.aspose.com/).


Jetzt verfügen Sie über das Wissen, Bildzeichnungen mithilfe von Aspose.Imaging für .NET nahtlos in Ihre .NET-Anwendungen zu integrieren. Diese kreative Fähigkeit öffnet die Tür zu einer Welt voller Möglichkeiten, Ihre Projekte mit Bildüberlagerungen zu verbessern. Wenn Sie Fragen haben oder weitere Hilfe benötigen, wenden Sie sich bitte an die Aspose.Imaging-Community im Support-Forum. Viel Spaß beim Codieren!

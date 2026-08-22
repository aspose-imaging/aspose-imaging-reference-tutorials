---
date: 2026-04-28
description: Erfahren Sie, wie Sie TIFF in PNG konvertieren und wie Sie TIFF in andere
  Rasterformate mit Aspose.Imaging für Java umwandeln. Schritt‑für‑Schritt‑Anleitung
  zur Bildbearbeitung.
keywords:
- tiff to png java
- how to convert tiff
- Aspose.Imaging Java
linktitle: Speichern von Frames in verschiedenen Rasterformaten
second_title: Aspose.Imaging Java Image Processing API
title: tiff zu png java – TIFF in PNG konvertieren und Frames in verschiedenen Rasterformaten
  speichern
url: /de/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# tiff zu png java – TIFF in PNG konvertieren und Frames in verschiedenen Rasterformaten speichern

Die Arbeit mit mehrseitigen TIFF‑Dateien ist ein gängiges Szenario in dokumentintensiven Anwendungen. Wenn Sie **tiff zu png konvertieren** möchten – oder einzelne Frames extrahieren und in anderen Rasterformaten speichern – macht Aspose.Imaging für Java den Prozess einfach und performant. In diesem Tutorial gehen wir Schritt für Schritt durch das Laden einer TIFF, das Durchlaufen ihrer Frames und das Speichern jedes einzelnen als PNG (Sie können später leicht zu BMP oder GIF wechseln). Am Ende sehen Sie auch, **wie man tiff** in eines der unterstützten Rasterformate mit nur wenigen Codezeilen konvertiert.

## Schnelle Antworten
- **Was bedeutet “convert tiff to png”?** Es bedeutet, jede Seite einer TIFF-Datei zu extrahieren und als PNG‑Rasterbild zu schreiben.  
- **Welche Bibliothek übernimmt das?** Aspose.Imaging für Java bietet vollständige Unterstützung für die Extraktion von TIFF‑Frames und die Konvertierung von Rasterformaten.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für die Entwicklung; für den Produktionseinsatz ist eine Volllizenz erforderlich.  
- **Kann ich statt PNG in BMP oder GIF speichern?** Ja – ersetzen Sie einfach `PngOptions` durch `BmpOptions` oder `GifOptions`.  
- **Welche Java-Version wird benötigt?** Java 8 oder höher wird empfohlen.

## Was ist “convert tiff to png”?
Das Konvertieren einer TIFF in PNG beinhaltet das Dekodieren des mehrseitigen TIFF, den Zugriff auf jeden Frame und das Kodieren dieses Frames in das PNG‑Format, das verlustfrei, web‑freundlich und weit verbreitet ist.

## Warum Aspose.Imaging für Java verwenden?
- **Breite Formatunterstützung** – Unterstützt TIFF, PNG, JPEG, BMP, GIF und vieles mehr.  
- **Keine nativen Abhängigkeiten** – Reines Java, einfach in jedes JVM‑Projekt zu integrieren.  
- **Hohe Leistung** – Optimiert für große Bilder und mehrseitige Dokumente.  
- **Einfache API** – Minimaler Code erforderlich, um komplexe Konvertierungen durchzuführen.

## Warum das wichtig ist
Viele Altsysteme speichern gescannte Dokumente als mehrseitige TIFFs, weil das Format archivfreundlich ist. Moderne Web‑ und Mobile‑Anwendungen bevorzugen jedoch PNG, BMP oder GIF für schnelles Rendering und die Erzeugung von Thumbnails. Das Konvertieren von TIFF‑Frames on‑the‑fly reduziert Speicherkosten, verbessert Ladezeiten und erweitert die Kompatibilität über Browser und Geräte hinweg.

## Voraussetzungen

1. **Java-Entwicklungsumgebung** – Stellen Sie sicher, dass das JDK installiert ist. Laden Sie es von der [Oracle-Website](https://www.oracle.com/java/technologies/javase-downloads) herunter, falls Sie dies noch nicht getan haben.  
2. **Aspose.Imaging für Java Bibliothek** – Greifen Sie auf die API‑Referenz in der [Dokumentation](https://reference.aspose.com/imaging/java/) zu. Laden Sie die Bibliothek von der [Download‑Seite](https://releases.aspose.com/imaging/java/) herunter. Eine kostenlose Testversion ist [hier](https://releases.aspose.com/) verfügbar, und eine Volllizenz kann [hier](https://purchase.aspose.com/buy) erworben werden.  
3. **Beispiel‑TIFF‑Bild** – Haben Sie ein mehrseitiges TIFF bereit zur Verarbeitung.

Jetzt, da die Voraussetzungen geklärt sind, tauchen wir in den Code ein.

## So konvertieren Sie TIFF zu PNG mit Aspose.Imaging für Java

### Pakete importieren
Zuerst importieren Sie die erforderlichen Aspose.Imaging‑Klassen.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

### Schritt 1: TIFF‑Bild laden
Initialisieren Sie das Datenverzeichnis und laden Sie die Quell‑TIFF‑Datei.

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

### Schritt 2: Frames in verschiedenen Rasterformaten speichern
Iterieren Sie über jeden Frame und **speichern das Bild als png**. Um **tiff zu bmp zu konvertieren** oder eine **tiff‑zu‑gif‑Konvertierung** durchzuführen, ersetzen Sie einfach `PngOptions` durch `BmpOptions` oder `GifOptions`.

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **Pro Tipp:** Behalten Sie den `try‑with‑resources`‑Block wie gezeigt bei, um sicherzustellen, dass die TIFF‑Datei nach der Verarbeitung ordnungsgemäß freigegeben wird.

## Häufige Anwendungsfälle
- **Dokumentenarchivierung:** Scannte TIFF‑Dokumente in PNG für die Web‑Vorschau konvertieren.  
- **Thumbnail‑Erstellung:** Den ersten Frame eines TIFF extrahieren und als kleines PNG‑Thumbnail speichern.  
- **Formatmigration:** Legacy‑TIFF‑Assets in moderne Formate wie BMP oder GIF überführen, um die Kompatibilität mit älteren Systemen zu gewährleisten.

## Fehlersuche & Tipps
- **Fehlende Frames:** Stellen Sie sicher, dass das Quell‑TIFF tatsächlich mehrere Seiten enthält; verwenden Sie `multiImage.getFrames().size()` zum Debuggen.  
- **Out‑of‑Memory‑Fehler:** Verarbeiten Sie große TIFFs seitenweise, wie gezeigt, anstatt die gesamte Datei in den Speicher zu laden.  
- **Qualitätskontrolle:** PNG ist verlustfrei; wenn Sie kleinere Dateien benötigen, sollten Sie JPEG‑Optionen mit Qualitäts‑Einstellungen in Betracht ziehen.

## Häufig gestellte Fragen

**Q1: Welche Rasterformate werden für das Speichern von Frames in Aspose.Imaging für Java unterstützt?**  
A1: Aspose.Imaging für Java unterstützt eine Vielzahl von Rasterformaten, darunter PNG, JPEG, BMP, GIF und mehr. Sie können das Format wählen, das am besten zu den Anforderungen Ihrer Anwendung passt.

**Q2: Kann ich mit Aspose.Imaging für Java weitere Bildoperationen durchführen?**  
A2: Ja, Aspose.Imaging für Java bietet ein umfassendes Set an Funktionen zur Bildbearbeitung, einschließlich Skalierung, Zuschneiden und Anwendung verschiedener Filter und Effekte. Es ist ein vielseitiges Werkzeug für alle Ihre Bildverarbeitungsanforderungen.

**Q3: Wie kann ich eine Volllizenz für Aspose.Imaging für Java erhalten?**  
A: Um eine Volllizenz für Aspose.Imaging für Java zu erwerben, besuchen Sie die [Kaufseite](https://purchase.aspose.com/buy). Dort finden Sie verschiedene Lizenzierungsoptionen, die zu Ihrem Projekt passen.

**Q4: Gibt es eine kostenlose Testversion für Aspose.Imaging für Java?**  
A: Ja, Sie können eine kostenlose Testversion von Aspose.Imaging für Java von der [Release‑Seite](https://releases.aspose.com/) erhalten. Diese Testversion ermöglicht es Ihnen, die Funktionen der Bibliothek zu erkunden, bevor Sie einen Kauf tätigen.

**Q5: Wo kann ich Unterstützung oder Hilfe zu Aspose.Imaging für Java erhalten?**  
A: Bei Fragen, Problemen oder Unterstützung zu Aspose.Imaging für Java können Sie das [Aspose Imaging‑Forum](https://forum.aspose.com/) besuchen. Die Community und das Support‑Team stehen Ihnen zur Verfügung.

---

**Zuletzt aktualisiert:** 2026-04-28  
**Getestet mit:** Aspose.Imaging für Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
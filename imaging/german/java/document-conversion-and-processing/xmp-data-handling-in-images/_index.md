---
"description": "Erfahren Sie, wie Sie XMP-Metadaten in Bildern mit Aspose.Imaging für Java verarbeiten. Betten Sie Metadaten ein und rufen Sie sie ab, um Ihre Bilddateien zu verbessern."
"linktitle": "XMP-Datenverarbeitung in Bildern"
"second_title": "Aspose.Imaging Java-Bildverarbeitungs-API"
"title": "XMP-Datenverarbeitung in Bildern mit Aspose.Imaging für Java"
"url": "/de/java/document-conversion-and-processing/xmp-data-handling-in-images/"
"weight": 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# XMP-Datenverarbeitung in Bildern mit Aspose.Imaging für Java

Aspose.Imaging für Java ist eine vielseitige und leistungsstarke Bibliothek für die Arbeit mit Bildern in verschiedenen Formaten. Dieses Tutorial führt Sie durch die Verarbeitung von XMP-Daten (Extensible Metadata Platform) in Bildern mit Aspose.Imaging für Java. XMP ist ein Standard zum Einbetten von Metadaten in Bilddateien und ermöglicht Ihnen die Speicherung wertvoller Informationen wie Autor, Beschreibung und mehr.

## Voraussetzungen

Stellen Sie vor dem Beginn sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Eine auf Ihrem Computer eingerichtete Java-Entwicklungsumgebung.
- Aspose.Imaging für Java-Bibliothek installiert. Sie können es herunterladen von der [Aspose.Imaging für Java-Website](https://releases.aspose.com/imaging/java/).
- Grundlegende Kenntnisse der Java-Programmierung.

## Pakete importieren

Importieren Sie zunächst die erforderlichen Pakete in Ihr Java-Projekt. Sie können die folgenden Importanweisungen am Anfang Ihres Codes hinzufügen:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.xmp.XmpPackage;
import com.aspose.imaging.xmp.XmpPacketWrapper;
import com.aspose.imaging.xmp.XmpMeta;
import com.aspose.imaging.xmp.photoshop.ColorMode;
import com.aspose.imaging.xmp.photoshop.PhotoshopPackage;
import com.aspose.imaging.xmp.dc.DublinCorePackage;
import com.aspose.imaging.xmp.header.XmpHeaderPi;
import com.aspose.imaging.xmp.trailer.XmpTrailerPi;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

Lassen Sie uns das Beispiel nun in eine Schritt-für-Schritt-Anleitung aufschlüsseln:

## Schritt 1: Bildgröße und TIFF-Optionen festlegen

Definieren Sie zunächst das Verzeichnis, in dem Ihr Bild gespeichert werden soll, und erstellen Sie ein Rechteck, um die Größe des Bildes festzulegen. In diesem Beispiel verwenden wir ein TIFF-Bild mit bestimmten Optionen.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## Schritt 2: Erstellen Sie ein neues Bild

Erstellen Sie nun ein neues Bild mit den angegebenen Optionen. Dieses Bild wird zum Speichern der XMP-Metadaten verwendet.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## Schritt 3: XMP-Header und -Trailer erstellen

Erstellen Sie Instanzen von XMP-Header und XMP-Trailer für Ihre XMP-Metadaten. Diese Header und Trailer helfen bei der Definition der Metadatenstruktur.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Schritt 4: XMP-Metainformationen erstellen

Erstellen Sie nun eine Instanz von XMP-Metadaten, um verschiedene Attribute festzulegen. Sie können Informationen wie Autor und Beschreibung hinzufügen.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Schritt 5: XMP-Paket-Wrapper erstellen

Erstellen Sie eine Instanz von XmpPacketWrapper, die den XMP-Header, den Trailer und die Metadaten enthält.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Schritt 6: Photoshop-Paket hinzufügen

Um Photoshop-spezifische Informationen zu speichern, erstellen Sie ein Photoshop-Paket und legen Sie dessen Attribute wie Stadt, Land und Farbmodus fest. Fügen Sie dieses Paket anschließend den XMP-Metadaten hinzu.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## Schritt 7: Dublin Core-Paket hinzufügen

Für allgemeinere Informationen wie Autor, Titel und weitere Werte erstellen Sie ein DublinCore-Paket und legen dessen Attribute fest. Fügen Sie dieses Paket auch den XMP-Metadaten hinzu.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## Schritt 8: Aktualisieren Sie die XMP-Metadaten im Bild

Aktualisieren Sie die XMP-Metadaten im Bild mithilfe der `setXmpData` Verfahren.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## Schritt 9: Speichern Sie das Bild

Sie können das Bild jetzt mit den eingebetteten XMP-Metadaten auf der Festplatte oder in einem Speicherstream speichern.

```java
    image.save(ms);
```

## Schritt 10: Laden Sie das Bild und rufen Sie die XMP-Metadaten ab

Um die XMP-Metadaten aus dem Bild abzurufen, laden Sie das Bild aus dem Speicherstream oder von der Festplatte und greifen Sie auf die XMP-Daten zu.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Paketdaten verwenden ...
        }
    }
}
```

Herzlichen Glückwunsch! Sie haben erfolgreich gelernt, wie Sie XMP-Daten in Bildern mit Aspose.Imaging für Java verarbeiten. Dadurch können Sie wertvolle Metadaten in Ihren Bilddateien speichern und abrufen.

## Abschluss

In diesem Tutorial haben wir die Arbeit mit XMP-Metadaten in Bildern mithilfe von Aspose.Imaging für Java untersucht. Mithilfe der Schritt-für-Schritt-Anleitung können Sie Metadaten einfach in Ihre Bilddateien einbetten und abrufen und so deren Informationen und Benutzerfreundlichkeit verbessern.

## Häufig gestellte Fragen

### F1: Was sind XMP-Metadaten?

A1: XMP (Extensible Metadata Platform) ist ein Standard zum Einbetten von Metadaten in verschiedene Dateitypen, einschließlich Bilder. Es ermöglicht Ihnen, Informationen wie Autor, Titel, Beschreibung und mehr direkt in der Datei zu speichern.

### F2: Warum sind XMP-Metadaten wichtig?

A2: XMP-Metadaten sind für die Organisation und Kategorisierung digitaler Assets unerlässlich. Sie helfen bei der Zuordnung von Eigentümern, der Beschreibung von Inhalten und dem Hinzufügen von Kontext zu Dateien wie Bildern, wodurch diese leichter zugänglich und aussagekräftiger werden.

### F3: Kann ich XMP-Metadaten bearbeiten, nachdem ich sie in ein Bild eingebettet habe?

A3: Ja, Sie können XMP-Metadaten nach dem Einbetten in ein Bild bearbeiten. Aspose.Imaging für Java bietet Tools zum Ändern und Aktualisieren von Metadatenattributen nach Bedarf.

### F4: Ist Aspose.Imaging für Java ein kostenloses Tool?

A4: Aspose.Imaging für Java bietet eine kostenlose Testversion an, für den vollen Funktionsumfang und die erweiterte Nutzung ist jedoch eine kostenpflichtige Lizenz erforderlich. Sie können die Optionen auf der [Aspose.Imaging für Java-Website](https://purchase.aspose.com/buy).

### F5: Wo erhalte ich Hilfe und Support für Aspose.Imaging für Java?

A5: Wenn Sie auf Probleme stoßen oder Fragen zu Aspose.Imaging für Java haben, können Sie die [Aspose.Imaging-Foren](https://forum.aspose.com/) für die Unterstützung und Anleitung durch die Community.



## Vollständiger Quellcode
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Geben Sie die Größe des Bildes an, indem Sie ein Rechteck definieren
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// Erstellen Sie das brandneue Bild nur zu Beispielzwecken
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// Erstellen Sie eine Instanz des XMP-Headers
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// Erstellen Sie eine Instanz von Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// Erstellen Sie eine Instanz der XMP-Metaklasse, um verschiedene Attribute festzulegen
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// Erstellen Sie eine Instanz von XmpPacketWrapper, die alle Metadaten enthält
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// Erstellen Sie eine Instanz des Photoshop-Pakets und legen Sie Photoshop-Attribute fest
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// Photoshop-Paket zu XMP-Metadaten hinzufügen
	xmpData.addPackage(photoshopPackage);
	// Erstellen Sie eine Instanz des DublinCore-Pakets und legen Sie DublinCore-Attribute fest
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// DublinCore-Paket zu XMP-Metadaten hinzufügen
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// XMP-Metadaten im Bild aktualisieren
	image.setXmpData(xmpData);
	// Speichern Sie das Bild auf der Festplatte oder im Speicherstream
	image.save(ms);
	// Laden Sie das Bild aus dem Speicherstream oder von der Festplatte, um die Metadaten zu lesen/abzurufen
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Abrufen der XMP-Metadaten
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Paketdaten verwenden ...
		}
	}
}
        
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
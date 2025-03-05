---
title: XMP-Datenverarbeitung in Bildern mit Aspose.Imaging für Java
linktitle: XMP-Datenverarbeitung in Bildern
second_title: Aspose.Imaging Java-Bildverarbeitungs-API
description: Erfahren Sie, wie Sie mit Aspose.Imaging für Java mit XMP-Metadaten in Bildern umgehen. Betten Sie Metadaten ein und rufen Sie sie ab, um Ihre Bilddateien zu verbessern.
type: docs
weight: 16
url: /de/java/document-conversion-and-processing/xmp-data-handling-in-images/
---
Aspose.Imaging für Java ist eine vielseitige und leistungsstarke Bibliothek für die Arbeit mit Bildern in verschiedenen Formaten. Dieses Tutorial führt Sie durch den Prozess der Verarbeitung von XMP-Daten (Extensible Metadata Platform) in Bildern mit Aspose.Imaging für Java. XMP ist ein Standard zum Einbetten von Metadaten in Bilddateien, der es Ihnen ermöglicht, wertvolle Informationen wie Autor, Beschreibung und mehr zu speichern.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Eine auf Ihrem Computer eingerichtete Java-Entwicklungsumgebung.
-  Aspose.Imaging für Java-Bibliothek installiert. Sie können es hier herunterladen[Aspose.Imaging für Java-Website](https://releases.aspose.com/imaging/java/).
- Ein grundlegendes Verständnis der Java-Programmierung.

## Pakete importieren

Beginnen Sie mit dem Importieren der erforderlichen Pakete in Ihr Java-Projekt. Sie können die folgenden Importanweisungen am Anfang Ihres Codes hinzufügen:

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

## Schritt 1: Geben Sie Bildgröße und TIFF-Optionen an

Definieren Sie zunächst das Verzeichnis, in dem Ihr Bild gespeichert wird, und erstellen Sie ein Rechteck, um die Größe des Bildes festzulegen. In diesem Beispiel verwenden wir ein TIFF-Bild mit bestimmten Optionen.

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

## Schritt 3: Erstellen Sie einen XMP-Header und -Trailer

Erstellen Sie Instanzen von XMP-Header und XMP-Trailer für Ihre XMP-Metadaten. Diese Header und Trailer helfen bei der Definition der Metadatenstruktur.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Schritt 4: Erstellen Sie XMP-Metainformationen

Erstellen Sie nun eine Instanz von XMP-Meta, um verschiedene Attribute festzulegen. Sie können Informationen wie den Autor und eine Beschreibung hinzufügen.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Schritt 5: Erstellen Sie einen XMP-Paket-Wrapper

Erstellen Sie eine Instanz von XmpPacketWrapper, die den XMP-Header, den Trailer und die Metainformationen enthält.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Schritt 6: Photoshop-Paket hinzufügen

Um Photoshop-spezifische Informationen zu speichern, erstellen Sie ein Photoshop-Paket und legen dessen Attribute wie Stadt, Land und Farbmodus fest. Fügen Sie dann dieses Paket zu den XMP-Metadaten hinzu.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## Schritt 7: Dublin-Kernpaket hinzufügen

Für allgemeinere Informationen wie Autor, Titel und zusätzliche Werte erstellen Sie ein DublinCore-Paket und legen seine Attribute fest. Fügen Sie dieses Paket auch zu den XMP-Metadaten hinzu.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## Schritt 8: XMP-Metadaten im Bild aktualisieren

 Aktualisieren Sie die XMP-Metadaten im Bild mithilfe von`setXmpData` Methode.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## Schritt 9: Speichern Sie das Bild

Sie können das Bild nun mit den eingebetteten XMP-Metadaten auf der Festplatte oder in einem Speicherstream speichern.

```java
    image.save(ms);
```

## Schritt 10: Laden Sie das Bild und rufen Sie die XMP-Metadaten ab

Um die XMP-Metadaten aus dem Bild abzurufen, laden Sie das Bild aus dem Speicherstream oder der Festplatte und greifen Sie auf die XMP-Daten zu.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Paketdaten verwenden ...
        }
    }
}
```

Glückwunsch! Sie haben erfolgreich gelernt, wie Sie mit Aspose.Imaging für Java mit XMP-Daten in Bildern umgehen. Dadurch können Sie wertvolle Metadaten in Ihren Bilddateien speichern und abrufen.

## Abschluss

In diesem Tutorial haben wir untersucht, wie man mit Aspose.Imaging für Java mit XMP-Metadaten in Bildern arbeitet. Wenn Sie der Schritt-für-Schritt-Anleitung folgen, können Sie ganz einfach Metadaten in Ihre Bilddateien einbetten und abrufen und so deren Informationen und Benutzerfreundlichkeit verbessern.

## FAQs

### F1: Was sind XMP-Metadaten?

A1: XMP (Extensible Metadata Platform) ist ein Standard zum Einbetten von Metadaten in verschiedene Dateitypen, einschließlich Bilder. Es ermöglicht Ihnen, Informationen wie Autor, Titel, Beschreibung und mehr in der Datei selbst zu speichern.

### F2: Warum sind XMP-Metadaten wichtig?

A2: XMP-Metadaten sind für die Organisation und Kategorisierung digitaler Assets unerlässlich. Es hilft bei der Zuweisung von Eigentumsrechten, der Beschreibung von Inhalten und dem Hinzufügen von Kontext zu Dateien wie Bildern, wodurch diese leichter zugänglich und aussagekräftiger werden.

### F3: Kann ich XMP-Metadaten bearbeiten, nachdem ich sie in ein Bild eingebettet habe?

A3: Ja, Sie können XMP-Metadaten bearbeiten, nachdem Sie sie in ein Bild eingebettet haben. Aspose.Imaging für Java bietet Tools zum Ändern und Aktualisieren von Metadatenattributen nach Bedarf.

### F4: Ist Aspose.Imaging für Java ein kostenloses Tool?

 A4: Aspose.Imaging für Java bietet eine kostenlose Testversion, für den vollen Funktionsumfang und die erweiterte Nutzung ist jedoch eine kostenpflichtige Lizenz erforderlich. Sie können die Optionen auf der erkunden[Aspose.Imaging für Java-Website](https://purchase.aspose.com/buy).

### F5: Wo erhalte ich Hilfe und Support für Aspose.Imaging für Java?

 A5: Wenn Sie auf Probleme stoßen oder Fragen zu Aspose.Imaging für Java haben, können Sie die besuchen[Aspose.Imaging-Foren](https://forum.aspose.com/) für gemeinschaftliche Unterstützung und Anleitung.



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
	// Erstellen Sie eine Instanz von XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// Erstellen Sie eine Instanz von Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// Erstellen Sie eine Instanz der XMP-Metaklasse, um verschiedene Attribute festzulegen
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	//Erstellen Sie eine Instanz von XmpPacketWrapper, die alle Metadaten enthält
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// Erstellen Sie eine Instanz des Photoshop-Pakets und legen Sie Photoshop-Attribute fest
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// Fügen Sie das Photoshop-Paket zu den XMP-Metadaten hinzu
	xmpData.addPackage(photoshopPackage);
	// Erstellen Sie eine Instanz des DublinCore-Pakets und legen Sie DublinCore-Attribute fest
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// Fügen Sie das DublinCore-Paket zu den XMP-Metadaten hinzu
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// Aktualisieren Sie die XMP-Metadaten im Bild
	image.setXmpData(xmpData);
	// Bild auf der Festplatte oder im Speicherstream speichern
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
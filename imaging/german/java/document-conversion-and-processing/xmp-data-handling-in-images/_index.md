---
date: 2026-05-18
description: Erfahren Sie, wie Sie die Java-Bildverarbeitungsbibliothek Aspose.Imaging
  verwenden, um XMP-Metadaten in Bildern einzubetten und abzurufen, mit Schritt‑für‑Schritt‑Code.
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: XMP-Datenverarbeitung in Bildern
schemas:
- author: Aspose
  dateModified: '2026-05-18'
  description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  headline: 'Java Image Processing Library: XMP with Aspose.Imaging'
  type: TechArticle
- description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  name: 'Java Image Processing Library: XMP with Aspose.Imaging'
  steps:
  - name: Specify Image Size and Tiff Options
    text: First, define the directory where your image will be stored and create a
      `Rectangle` to specify the size of the image. In this example, we use a TIFF
      image with certain options. `TiffOptions` configures format‑specific settings
      for the TIFF image.
  - name: Create a New Image
    text: Now, create a new image with the specified options. This image will be used
      to store the XMP metadata. `TiffImage` represents a TIFF image object, and `TiffFrame`
      defines an individual frame within it.
  - name: Create XMP Header and Trailer
    text: Create instances of XMP‑Header and XMP‑Trailer for your XMP metadata. These
      headers and trailers help define the metadata structure. `XmpHeaderPi` and `XmpTrailerPi`
      represent the XMP packet’s opening and closing sections.
  - name: Create XMP Meta Information
    text: Now, create an instance of XMP meta to set different attributes. You can
      add information like the author and description. `XmpMeta` holds the core metadata
      fields such as author and description.
  - name: Create XMP Packet Wrapper
    text: '`XmpPacketWrapper` is the container that holds the XMP header, trailer,
      and meta information in a single packet. It ensures the packet conforms to the
      XMP specification. `XmpPacketWrapper` packages the header, meta, and trailer
      into a single XMP packet.'
  - name: Add Photoshop Package
    text: To store Photoshop‑specific information, create a Photoshop package and
      set its attributes, such as city, country, and color mode. Then, add this package
      to the XMP metadata. `PhotoshopPackage` stores Photoshop‑specific metadata like
      city, country, and color mode.
  - name: Add Dublin Core Package
    text: For more general information, like author, title, and additional values,
      create a DublinCore package and set its attributes. Add this package to the
      XMP metadata as well. `DublinCorePackage` contains standard Dublin Core fields
      such as title, creator, and keywords.
  - name: Update XMP Metadata in the Image
    text: Update the XMP metadata into the image using the `setXmpData` method. This
      call writes the XMP packet into the image’s metadata section. `setXmpData` writes
      the XMP packet into the image’s metadata section.
  - name: Save the Image
    text: You can now save the image with the embedded XMP metadata on the disk or
      in a memory stream.
  - name: Load the Image and Retrieve XMP Metadata
    text: To retrieve the XMP metadata from the image, load the image from the memory
      stream or disk and access the XMP data via the `getXmpData` method. `getXmpData`
      reads the embedded XMP packet from the image. Congratulations! You've successfully
      learned how to handle XMP data in images using Aspose.Imagin
  type: HowTo
- questions:
  - answer: XMP is an XML‑based standard for embedding descriptive information directly
      inside files, enabling consistent metadata across applications.
    question: What is XMP metadata?
  - answer: It lets you tag images with author, copyright, keywords, and custom data,
      improving searchability and asset management without external databases.
    question: Why is XMP metadata important?
  - answer: Yes, Aspose.Imaging for Java provides methods to modify existing XMP packets
      and write them back to the file.
    question: Can I edit XMP metadata after embedding it in an image?
  - answer: A free trial is available for evaluation, but a paid license is required
      for production use. You can explore options on the [Aspose.Imaging for Java
      website](https://purchase.aspose.com/buy).
    question: Is Aspose.Imaging for Java a free tool?
  - answer: Visit the [Aspose.Imaging forums](https://forum.aspose.com/) for community
      assistance, or contact Aspose support directly for paid‑license customers.
    question: Where can I get help and support for Aspose.Imaging for Java?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: 'Java-Bildverarbeitungsbibliothek: XMP mit Aspose.Imaging'
url: /de/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# XMP-Datenverarbeitung in Bildern mit Aspose.Imaging für Java

Aspose.Imaging ist eine **java image processing library**, die es Ihnen ermöglicht, mit Dutzenden von Raster- und Vektorformaten zu arbeiten. In diesem Tutorial lernen Sie, wie Sie XMP (Extensible Metadata Platform)-Daten in Bildern mit Aspose.Imaging für Java einbetten und abrufen. Am Ende können Sie Autor, Beschreibung und benutzerdefinierte Metadaten direkt in Ihren Bilddateien speichern, wodurch sie durchsuchbar und selbsterklärend werden.

## Schnelle Antworten
- **Was ist XMP?** XMP ist ein standardisiertes XML‑basiertes Format zum Einbetten von Metadaten in Dateien wie Bilder, PDFs und Videos.  
- **Welche Bibliothek verarbeitet XMP in Java?** Aspose.Imaging for Java bietet eine vollständige API zum Lesen und Schreiben von XMP‑Paketen.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Wie viele Bildformate werden unterstützt?** Über 150 Formate, darunter TIFF, JPEG, PNG, PSD und RAW.  
- **Kann ich große Bilder verarbeiten?** Ja – die Bibliothek kann Dateien bis zu 2 GB verarbeiten, ohne das gesamte Bild in den Speicher zu laden.

## Was ist XMP-Metadaten?
XMP-Metadaten sind ein XML‑basiertes Standard, das beschreibende Informationen direkt in digitale Dateien einbettet. Es ermöglicht eine konsistente Speicherung von Autor, Urheberrecht, Schlüsselwörtern und benutzerdefinierten Daten über Anwendungen hinweg. Da es XML ist, kann XMP mit benutzerdefinierten Namespaces erweitert werden, sodass Entwickler proprietäre Felder hinzufügen können, während die Kompatibilität mit Werkzeugen, die das Kernschema verstehen, erhalten bleibt. Dies macht XMP ideal für langfristiges Asset‑Management und plattformübergreifende Interoperabilität.

## Warum eine Java image processing library für XMP verwenden?
Aspose.Imaging für Java unterstützt **150+ Bildformate** und kann Multi‑Gigabyte‑Dateien in einem Streaming‑Modus verarbeiten, wodurch der Speicherverbrauch im Vergleich zum naiven Laden um bis zu 80 % reduziert wird. Die API stellt zudem sicher, dass XMP‑Pakete den Standards entsprechen, was die Kompatibilität mit Adobe Photoshop, Lightroom und anderen Werkzeugen gewährleistet.

## Voraussetzungen

- Eine Java‑Entwicklungsumgebung auf Ihrem Computer eingerichtet.  
- Aspose.Imaging for Java Bibliothek installiert. Sie können sie von der [Aspose.Imaging for Java website](https://releases.aspose.com/imaging/java/) herunterladen.  
- Grundlegendes Verständnis der Java‑Programmierung.

## Importieren von Paketen

Beginnen Sie damit, die notwendigen Pakete in Ihr Java‑Projekt zu importieren. Sie können die folgenden Import‑Anweisungen am Anfang Ihres Codes hinzufügen:

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

Nun zerlegen wir das Beispiel in eine Schritt‑für‑Schritt‑Anleitung:

## Wie bettet man XMP-Metadaten mit einer Java image processing library ein?

Laden Sie Ihr Bild, erstellen Sie ein XMP‑Paket, hängen Sie das Paket an das Bild an und speichern Sie – alles in wenigen prägnanten Zeilen. Die `setXmpData`‑Methode von Aspose.Imaging schreibt das Paket direkt in die Datei, ohne dass eine separate Metadatendatei erforderlich ist. Der Vorgang funktioniert sowohl mit dateibasierten als auch mit streambasierten Bildern und ist somit für Web‑Dienste und Batch‑Jobs geeignet.

### Schritt 1: Bildgröße und Tiff-Optionen festlegen

Zuerst definieren Sie das Verzeichnis, in dem Ihr Bild gespeichert wird, und erstellen ein `Rectangle`, um die Größe des Bildes festzulegen. In diesem Beispiel verwenden wir ein TIFF‑Bild mit bestimmten Optionen. `TiffOptions` konfiguriert format‑spezifische Einstellungen für das TIFF‑Bild.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### Schritt 2: Neues Bild erstellen

Erstellen Sie nun ein neues Bild mit den angegebenen Optionen. Dieses Bild wird verwendet, um die XMP‑Metadaten zu speichern. `TiffImage` repräsentiert ein TIFF‑Bildobjekt, und `TiffFrame` definiert einen einzelnen Frame darin.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### Schritt 3: XMP-Header und -Trailer erstellen

Erstellen Sie Instanzen von XMP‑Header und XMP‑Trailer für Ihre XMP‑Metadaten. Diese Header und Trailer helfen, die Metadatenstruktur zu definieren. `XmpHeaderPi` und `XmpTrailerPi` repräsentieren die öffnenden bzw. schließenden Abschnitte des XMP‑Pakets.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### Schritt 4: XMP-Meta-Informationen erstellen

Erstellen Sie nun eine Instanz von XMP‑Meta, um verschiedene Attribute festzulegen. Sie können Informationen wie Autor und Beschreibung hinzufügen. `XmpMeta` enthält die Kern‑Metadatenfelder wie Autor und Beschreibung.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### Schritt 5: XMP-Packet-Wrapper erstellen

`XmpPacketWrapper` ist der Container, der den XMP-Header, Trailer und die Meta-Informationen in einem einzigen Paket hält. Er stellt sicher, dass das Paket der XMP-Spezifikation entspricht. `XmpPacketWrapper` verpackt Header, Meta und Trailer zu einem einzigen XMP-Paket.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### Schritt 6: Photoshop-Paket hinzufügen

Um Photoshop-spezifische Informationen zu speichern, erstellen Sie ein Photoshop-Paket und setzen dessen Attribute, wie Stadt, Land und Farbmodus. Anschließend fügen Sie dieses Paket zu den XMP-Metadaten hinzu. `PhotoshopPackage` speichert Photoshop-spezifische Metadaten wie Stadt, Land und Farbmodus.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### Schritt 7: Dublin-Core-Paket hinzufügen

Für allgemeinere Informationen, wie Autor, Titel und zusätzliche Werte, erstellen Sie ein DublinCore-Paket und setzen dessen Attribute. Fügen Sie dieses Paket ebenfalls zu den XMP-Metadaten hinzu. `DublinCorePackage` enthält standardisierte Dublin-Core-Felder wie Titel, Ersteller und Schlüsselwörter.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### Schritt 8: XMP-Metadaten im Bild aktualisieren

Aktualisieren Sie die XMP-Metadaten im Bild mithilfe der `setXmpData`-Methode. Dieser Aufruf schreibt das XMP-Paket in den Metadaten-Abschnitt des Bildes. `setXmpData` schreibt das XMP-Paket in den Metadaten-Abschnitt des Bildes.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### Schritt 9: Bild speichern

Sie können das Bild nun mit den eingebetteten XMP-Metadaten auf der Festplatte oder in einem Speicher-Stream speichern.

```java
    image.save(ms);
```

### Schritt 10: Bild laden und XMP-Metadaten abrufen

Um die XMP-Metadaten aus dem Bild abzurufen, laden Sie das Bild aus dem Speicher-Stream oder von der Festplatte und greifen über die `getXmpData`-Methode auf die XMP-Daten zu. `getXmpData` liest das eingebettete XMP-Paket aus dem Bild.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

Herzlichen Glückwunsch! Sie haben erfolgreich gelernt, wie Sie XMP-Daten in Bildern mit Aspose.Imaging für Java verarbeiten. Damit können Sie wertvolle Metadaten in Ihren Bilddateien speichern und abrufen.

## Häufige Probleme und Lösungen

- **Metadaten erscheinen nicht in Photoshop:** Stellen Sie sicher, dass das XMP-Paket dem korrekten XML-Schema folgt; Aspose.Imaging validiert es automatisch, aber benutzerdefinierte Namespaces müssen möglicherweise registriert werden.  
- **Große TIFF-Dateien verursachen OutOfMemoryError:** Verwenden Sie `TiffOptions` mit `Compression` auf `LZW` gesetzt und aktivieren Sie das Streaming (`loadOptions.setBufferSize`), um den Speicherverbrauch gering zu halten.  
- **Unerwartete Zeichenkodierung:** XMP erwartet UTF-8; übergeben Sie stets Zeichenketten mit `StandardCharsets.UTF_8`, um fehlerhafte Daten zu vermeiden.

## Häufig gestellte Fragen

**Q: Was ist XMP-Metadaten?**  
A: XMP ist ein XML-basierter Standard zum Einbetten beschreibender Informationen direkt in Dateien, wodurch konsistente Metadaten über Anwendungen hinweg ermöglicht werden.

**Q: Warum sind XMP-Metadaten wichtig?**  
A: Sie ermöglichen das Taggen von Bildern mit Autor, Urheberrecht, Schlüsselwörtern und benutzerdefinierten Daten, was die Durchsuchbarkeit und das Asset-Management ohne externe Datenbanken verbessert.

**Q: Kann ich XMP-Metadaten nach dem Einbetten in ein Bild bearbeiten?**  
A: Ja, Aspose.Imaging für Java bietet Methoden zum Ändern vorhandener XMP-Pakete und zum Zurückschreiben in die Datei.

**Q: Ist Aspose.Imaging für Java ein kostenloses Tool?**  
A: Eine kostenlose Testversion steht zur Evaluierung bereit, aber für den Produktionseinsatz ist eine kostenpflichtige Lizenz erforderlich. Optionen können Sie auf der [Aspose.Imaging for Java website](https://purchase.aspose.com/buy) einsehen.

**Q: Wo kann ich Hilfe und Support für Aspose.Imaging für Java erhalten?**  
A: Besuchen Sie die [Aspose.Imaging forums](https://forum.aspose.com/) für Community-Unterstützung oder kontaktieren Sie den Aspose-Support direkt für Kunden mit kostenpflichtiger Lizenz.

## Fazit

In diesem Tutorial haben wir untersucht, wie man mit XMP-Metadaten in Bildern mithilfe von Aspose.Imaging für Java, einer führenden **java image processing library**, arbeitet. Durch Befolgen der Schritt-für-Schritt-Anleitung können Sie XMP-Daten einfach einbetten, aktualisieren und abrufen und so Ihre digitalen Assets mit durchsuchbaren, standardkonformen Metadaten anreichern.

---

**Zuletzt aktualisiert:** 2026-05-18  
**Getestet mit:** Aspose.Imaging for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [Java-Bildverarbeitung meistern: EXIF-Daten mit Aspose.Imaging ändern](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [Java-Bildverarbeitung mit Aspose.Imaging: Laden, Verbessern & Speichern von Bildern](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [Fortgeschrittene Java-Bildverarbeitung mit der Aspose.Imaging-Bibliothek](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Specify the size of image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// create the brand new image just for sample purposes
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// create an instance of XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// create an instance of Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// create an instance of XMP meta class to set different attributes
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// create an instance of XmpPacketWrapper that contains all metadata
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// create an instance of Photoshop package and set photoshop attributes
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// add photoshop package into XMP metadata
	xmpData.addPackage(photoshopPackage);
	// create an instance of DublinCore package and set dublinCore attributes
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// add dublinCore Package into XMP metadata
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// update XMP metadata into image
	image.setXmpData(xmpData);
	// Save image on the disk or in memory stream
	image.save(ms);
	// Load the image from memory stream or from disk to read/get the metadata
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Getting the XMP metadata
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Use package data ...
		}
	}
}
        
```
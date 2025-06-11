---
"date": "2025-06-04"
"description": "Erfahren Sie, wie Sie DICOM-Bilder mit Aspose.Imaging für Java einfach in das BMP-Format konvertieren und deren Größe ändern. Ideal für die medizinische Bildarchivierung und Webanzeige."
"title": "Konvertieren Sie DICOM in BMP in Java mit Aspose.Imaging – Eine vollständige Anleitung"
"url": "/de/java/format-conversion-export/aspose-imaging-java-dicom-to-bmp-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# So laden und speichern Sie DICOM-Bilder als BMP mit Aspose.Imaging Java

## Einführung

In der digitalen Bildgebung ist die Verwaltung medizinischer Bilder von entscheidender Bedeutung. Oft müssen Fachleute diese Bilder von einem Format in ein anderes konvertieren und dabei ihre Integrität wahren. Dieses Tutorial führt Sie durch die Verwendung von Aspose.Imaging für Java, um ein DICOM-Bild zu laden und im BMP-Format erneut zu speichern. Sie erfahren außerdem, wie Sie die Höhe Ihrer DICOM-Bilder proportional anpassen.

**Was Sie lernen werden:**

- So konvertieren Sie DICOM-Bilder mit Aspose.Imaging Java in BMP
- Techniken zum Ändern der Größe von DICOM-Bildern unter Beibehaltung der Proportionen
- Einrichten von Aspose.Imaging für Java in Ihrer Entwicklungsumgebung

Bevor wir mit der Implementierung beginnen, stellen wir sicher, dass Sie die Voraussetzungen erfüllt haben. 

## Voraussetzungen

Um diesem Tutorial effektiv folgen zu können, benötigen Sie:

- **Aspose.Imaging-Bibliothek**: Stellen Sie sicher, dass Sie Version 25.5 oder höher haben.
- **Java Development Kit (JDK)**: Aus Kompatibilitätsgründen wird Version 8 oder höher empfohlen.
- **IDE-Einrichtung**Verwenden Sie eine IDE wie IntelliJ IDEA oder Eclipse, um Ihren Java-Code zu schreiben und zu testen.

## Einrichten von Aspose.Imaging für Java

Richten Sie zunächst Aspose.Imaging in Ihrem Projekt ein. Sie können Maven oder Gradle als Build-Tool verwenden.

**Maven**
```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

**Gradle**
```gradle
implementation 'com.aspose:aspose-imaging:25.5'
```

Alternativ können Sie die Bibliothek direkt herunterladen von [Aspose.Imaging für Java-Releases](https://releases.aspose.com/imaging/java/).

### Lizenzerwerb

Um mit Aspose.Imaging zu beginnen, können Sie:

- **Kostenlose Testversion**: Testen Sie die Funktionen mit einer begrenzten Testversion.
- **Temporäre Lizenz**: Erwerben Sie eine temporäre Lizenz, um alle Funktionen zu erkunden.
- **Kaufen**: Für eine erweiterte Nutzung sollten Sie den Kauf einer Lizenz in Erwägung ziehen.

**Initialisierung und Einrichtung:**

Initialisieren Sie die Bibliothek nach der Installation in Ihrer Java-Anwendung. Dazu müssen Sie Dateiverzeichnisse einrichten und sicherstellen, dass die Aspose.Imaging-Bibliotheken korrekt referenziert werden.

## Implementierungshandbuch

Wir unterteilen unsere Implementierung in zwei Hauptfunktionen:

### DICOM-Bild als BMP laden und erneut speichern

#### Überblick

Diese Funktion zeigt, wie ein DICOM-Bild von der Festplatte geladen und im BMP-Format gespeichert wird, sodass es für nicht-medizinische Anwendungen oder Systeme zugänglich ist, die grundlegende Bildformate erfordern.

#### Schrittweise Implementierung

1. **Verzeichnisse einrichten**

   Definieren Sie Ihre Eingabe- und Ausgabeverzeichnisse, in denen sich die DICOM-Datei befindet und wo die BMP-Datei gespeichert werden soll.
   ```java
   String dataDir = "YOUR_DOCUMENT_DIRECTORY";
   String inputFile = dataDir + "image.dcm";
   String outputFile = "YOUR_OUTPUT_DIRECTORY" + "ResizedOutput.bmp";
   ```

2. **DICOM-Bild laden und speichern**

   Verwenden `DicomImage` von Aspose.Imaging, um das Bild zu laden und es dann im BMP-Format zu speichern.
   ```java
   try (DicomImage image = (DicomImage) Image.load(inputFile)) {
       // Speichern Sie das Bild als BMP-Datei.
       image.save(outputFile, new BmpOptions());
   }
   ```

3. **Parameter erklären**

   - `inputFile`: Pfad zu Ihrer DICOM-Datei.
   - `outputFile`: Zielpfad für die BMP-Ausgabe.
   - `BmpOptions()`: Konfigurationseinstellungen für das BMP-Format.

### Höhe proportional anpassen

#### Überblick

Mit dieser Funktion können Sie die Höhe eines DICOM-Bildes proportional ändern, das Seitenverhältnis beibehalten und es als BMP-Datei speichern.

#### Schrittweise Implementierung

1. **Laden Sie das DICOM-Bild**

   Beginnen Sie, indem Sie Ihr DICOM-Bild mit Aspose.Imaging laden.
   ```java
   String inputFile = dataDir + "image.dcm";
   String outputFile = "YOUR_OUTPUT_DIRECTORY" + "ResizeHeightProportionally_out.bmp";

   try (DicomImage image = (DicomImage) Image.load(inputFile)) {
       // Passen Sie die Höhe proportional auf 100 Pixel an.
       image.resizeHeightProportionally(100, ResizeType.AdaptiveResample);
       
       // Speichern Sie das skalierte Bild im BMP-Format.
       image.save(outputFile, new BmpOptions());
   }
   ```

2. **Parameter und Methoden**

   - `resizeHeightProportionally(100, ResizeType.AdaptiveResample)`: Bei dieser Methode wird die Höhe auf 100 Pixel angepasst, während das Seitenverhältnis durch adaptives Resampling zur Qualitätssicherung beibehalten wird.

## Praktische Anwendungen

Hier sind einige reale Szenarien, in denen diese Funktionen angewendet werden können:

1. **Medizinische Bildarchivierung**: Konvertieren und skalieren Sie DICOM-Bilder für eine einfachere Speicherung in nicht-medizinischen Systemen.
2. **Webanzeige medizinischer Bilder**: Verwenden Sie das BMP-Format, um medizinische Bilder in Webanwendungen anzuzeigen und so die Dateigröße zu reduzieren, ohne die Qualität zu beeinträchtigen.
3. **Plattformübergreifende Kompatibilität**: Vereinfachen Sie den Bildaustausch zwischen unterschiedlicher Software, die möglicherweise keine DICOM-Formate unterstützt.

## Überlegungen zur Leistung

Bei der Arbeit mit Aspose.Imaging für Java:

- **Bildgrößen optimieren**Bevor Sie große DICOM-Dateien konvertieren, sollten Sie deren Größe ändern, um die Verarbeitungszeit und den Speicherverbrauch zu reduzieren.
- **Effizientes Speichermanagement**: Nutzen Sie Try-with-Resources, um den Speicher beim Umgang mit Bilddaten effektiv zu verwalten.
- **Stapelverarbeitung**: Wenn Sie mehrere Bilder verarbeiten, automatisieren Sie den Prozess in Stapeln, um die Effizienz zu verbessern.

## Abschluss

In diesem Tutorial haben Sie gelernt, wie Sie DICOM-Bilder laden und mit Aspose.Imaging für Java in das BMP-Format konvertieren. Außerdem haben wir die Größenänderung von Bildern unter Beibehaltung ihrer Proportionen behandelt. Mit diesen Kenntnissen können Sie medizinische Bildgebungslösungen effektiver in verschiedene Anwendungen integrieren.

**Nächste Schritte:**

- Experimentieren Sie mit zusätzlichen Bildbearbeitungsfunktionen von Aspose.Imaging.
- Erkunden Sie Integrationsmöglichkeiten mit anderen Systemen wie Gesundheitsdatenbanken oder Webplattformen.

## FAQ-Bereich

1. **Was ist Aspose.Imaging?**
   - Aspose.Imaging ist eine leistungsstarke Bibliothek zur Bildverarbeitung in Java, die verschiedene Formate unterstützt, darunter DICOM und BMP.

2. **Kann ich Aspose.Imaging verwenden, ohne eine Lizenz zu erwerben?**
   - Ja, Sie können mit einer kostenlosen Testversion beginnen oder eine vorübergehende Lizenz erwerben, um die Funktionen zu erkunden.

3. **Welche Bildformate werden von Aspose.Imaging unterstützt?**
   - Es unterstützt eine Vielzahl von Formaten, darunter unter anderem JPEG, PNG, GIF, BMP und DICOM.

4. **Wie verarbeite ich große DICOM-Dateien mit Aspose.Imaging?**
   - Erwägen Sie, die Größe von Bildern vor der Verarbeitung zu ändern, um die Speichernutzung effizient zu verwalten.

5. **Ist es möglich, diese Bibliothek in bestehende Java-Anwendungen zu integrieren?**
   - Ja, Aspose.Imaging kann mithilfe von Maven- oder Gradle-Abhängigkeiten nahtlos in Ihre aktuellen Projekte integriert werden.

## Ressourcen

- [Dokumentation](https://reference.aspose.com/imaging/java/)
- [Download-Bibliothek](https://releases.aspose.com/imaging/java/)
- [Kaufoptionen](https://purchase.aspose.com/buy)
- [Kostenlose Testversion](https://releases.aspose.com/imaging/java/)
- [Temporäre Lizenz](https://purchase.aspose.com/temporary-license/)
- [Support-Forum](https://forum.aspose.com/c/imaging/10)

Mit dieser Anleitung sind Sie nun bestens gerüstet, um DICOM-Bilder mit Aspose.Imaging für Java zu verarbeiten. Viel Spaß beim Programmieren!

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
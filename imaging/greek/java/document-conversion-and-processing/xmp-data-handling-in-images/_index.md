---
date: 2026-05-18
description: Μάθετε πώς να χρησιμοποιείτε τη βιβλιοθήκη επεξεργασίας εικόνας Java
  Aspose.Imaging για την ενσωμάτωση και ανάκτηση μεταδεδομένων XMP σε εικόνες, με
  βήμα‑βήμα κώδικα.
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: Διαχείριση Δεδομένων XMP σε Εικόνες
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
title: 'Βιβλιοθήκη Επεξεργασίας Εικόνας Java: XMP με Aspose.Imaging'
url: /el/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Διαχείριση δεδομένων XMP σε εικόνες με Aspose.Imaging για Java

Aspose.Imaging είναι μια **java image processing library** που σας επιτρέπει να εργάζεστε με δεκάδες μορφές raster και vector. Σε αυτό το tutorial θα μάθετε πώς να ενσωματώνετε και να ανακτάτε δεδομένα XMP (Extensible Metadata Platform) σε εικόνες χρησιμοποιώντας το Aspose.Imaging για Java. Στο τέλος, θα μπορείτε να αποθηκεύετε συγγραφέα, περιγραφή και προσαρμοσμένα μεταδεδομένα απευθείας μέσα στα αρχεία εικόνας, καθιστώντας τα αναζητήσιμα και αυτο‑περιγραφικά.

## Σύντομες Απαντήσεις
- **Τι είναι το XMP;** Το XMP είναι μια τυποποιημένη μορφή βασισμένη σε XML για ενσωμάτωση μεταδεδομένων μέσα σε αρχεία όπως εικόνες, PDF και βίντεο.  
- **Ποια βιβλιοθήκη διαχειρίζεται το XMP σε Java;** Το Aspose.Imaging για Java παρέχει ένα πλήρες API για ανάγνωση και εγγραφή πακέτων XMP.  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.  
- **Πόσες μορφές εικόνας υποστηρίζονται;** Πάνω από 150 μορφές, συμπεριλαμβανομένων TIFF, JPEG, PNG, PSD και RAW.  
- **Μπορώ να επεξεργαστώ μεγάλες εικόνες;** Ναι – η βιβλιοθήκη μπορεί να διαχειριστεί αρχεία έως 2 GB χωρίς να φορτώνει ολόκληρη την εικόνα στη μνήμη.

## Τι είναι τα μεταδεδομένα XMP;
Τα μεταδεδομένα XMP είναι ένα πρότυπο βασισμένο σε XML που ενσωματώνει περιγραφικές πληροφορίες απευθείας σε ψηφιακά αρχεία. Επιτρέπει συνεπή αποθήκευση συγγραφέα, πνευματικών δικαιωμάτων, λέξεων‑κλειδιά και προσαρμοσμένων δεδομένων σε διάφορες εφαρμογές. Επειδή είναι XML, το XMP μπορεί να επεκταθεί με προσαρμοσμένα namespaces, επιτρέποντας στους προγραμματιστές να προσθέτουν ιδιόκτητα πεδία ενώ παραμένουν συμβατά με εργαλεία που κατανοούν το βασικό σχήμα. Αυτό το καθιστά ιδανικό για μακροπρόθεσμη διαχείριση περιουσιακών στοιχείων και διαλειτουργικότητα μεταξύ εφαρμογών.

## Γιατί να χρησιμοποιήσετε μια Java image processing library για XMP;
Το Aspose.Imaging για Java υποστηρίζει **150+ μορφές εικόνας** και μπορεί να επεξεργαστεί αρχεία πολλαπλών gigabyte με ροή, μειώνοντας τη χρήση μνήμης έως και 80 % σε σύγκριση με την απλή φόρτωση. Το API επίσης εγγυάται ότι τα πακέτα XMP παραμένουν σύμφωνα με τα πρότυπα, εξασφαλίζοντας συμβατότητα με Adobe Photoshop, Lightroom και άλλα εργαλεία.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε τα παρακάτω:

- Ένα περιβάλλον ανάπτυξης Java εγκατεστημένο στον υπολογιστή σας.  
- Η βιβλιοθήκη Aspose.Imaging για Java εγκατεστημένη. Μπορείτε να τη κατεβάσετε από το [Aspose.Imaging for Java website](https://releases.aspose.com/imaging/java/).  
- Βασική κατανόηση του προγραμματισμού Java.

## Εισαγωγή Πακέτων

Ξεκινήστε εισάγοντας τα απαραίτητα πακέτα στο έργο Java σας. Μπορείτε να προσθέσετε τις παρακάτω δηλώσεις import στην αρχή του κώδικά σας:

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

Τώρα, ας αναλύσουμε το παράδειγμα σε έναν οδηγό βήμα‑βήμα:

## Πώς να ενσωματώσετε μεταδεδομένα XMP χρησιμοποιώντας μια Java image processing library;

Φορτώστε την εικόνα σας, δημιουργήστε ένα πακέτο XMP, επισυνάψτε το πακέτο στην εικόνα και αποθηκεύστε – όλα σε λίγες σύντομες γραμμές. Η μέθοδος `setXmpData` του Aspose.Imaging γράφει το πακέτο απευθείας στο αρχείο χωρίς να απαιτείται ξεχωριστό αρχείο μεταδεδομένων. Η διαδικασία λειτουργεί τόσο με εικόνες βασισμένες σε αρχείο όσο και με εικόνες βασισμένες σε ροή, καθιστώντας την κατάλληλη για web services και batch jobs.

### Βήμα 1: Καθορίστε το Μέγεθος της Εικόνας και τις Επιλογές Tiff

Πρώτα, ορίστε τον φάκελο όπου θα αποθηκευτεί η εικόνα σας και δημιουργήστε ένα `Rectangle` για να καθορίσετε το μέγεθος της εικόνας. Σε αυτό το παράδειγμα, χρησιμοποιούμε μια εικόνα TIFF με ορισμένες επιλογές. Το `TiffOptions` διαμορφώνει ρυθμίσεις ειδικές για τη μορφή TIFF.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### Βήμα 2: Δημιουργία Νέας Εικόνας

Τώρα, δημιουργήστε μια νέα εικόνα με τις καθορισμένες επιλογές. Αυτή η εικόνα θα χρησιμοποιηθεί για την αποθήκευση των μεταδεδομένων XMP. Το `TiffImage` αντιπροσωπεύει ένα αντικείμενο εικόνας TIFF, και το `TiffFrame` ορίζει ένα μεμονωμένο πλαίσιο μέσα σε αυτήν.

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### Βήμα 3: Δημιουργία XMP Header και Trailer

Δημιουργήστε στιγμιότυπα του XMP‑Header και του XMP‑Trailer για τα μεταδεδομένα XMP σας. Αυτά τα headers και trailers βοηθούν στον ορισμό της δομής των μεταδεδομένων. Τα `XmpHeaderPi` και `XmpTrailerPi` αντιπροσωπεύουν τις αρχικές και τελικές ενότητες του πακέτου XMP.

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### Βήμα 4: Δημιουργία Πληροφοριών XMP Meta

Τώρα, δημιουργήστε ένα στιγμιότυπο του XMP meta για να ορίσετε διαφορετικά χαρακτηριστικά. Μπορείτε να προσθέσετε πληροφορίες όπως ο συγγραφέας και η περιγραφή. Το `XmpMeta` περιέχει τα βασικά πεδία μεταδεδομένων όπως ο συγγραφέας και η περιγραφή.

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### Βήμα 5: Δημιουργία XMP Packet Wrapper

Το `XmpPacketWrapper` είναι ο container που κρατά το header, το trailer και τις meta πληροφορίες του XMP σε ένα ενιαίο πακέτο. Διασφαλίζει ότι το πακέτο συμμορφώνεται με την προδιαγραφή XMP. Το `XmpPacketWrapper` συσκευάζει το header, το meta και το trailer σε ένα ενιαίο πακέτο XMP.

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### Βήμα 6: Προσθήκη Πακέτου Photoshop

Για αποθήκευση πληροφοριών ειδικών για το Photoshop, δημιουργήστε ένα Photoshop package και ορίστε τα χαρακτηριστικά του, όπως πόλη, χώρα και λειτουργία χρώματος. Στη συνέχεια, προσθέστε αυτό το πακέτο στα μεταδεδομένα XMP. Το `PhotoshopPackage` αποθηκεύει μεταδεδομένα ειδικά για το Photoshop όπως πόλη, χώρα και λειτουργία χρώματος.

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### Βήμα 7: Προσθήκη Πακέτου Dublin Core

Για πιο γενικές πληροφορίες, όπως συγγραφέας, τίτλος και πρόσθετες τιμές, δημιουργήστε ένα DublinCore package και ορίστε τα χαρακτηριστικά του. Προσθέστε αυτό το πακέτο επίσης στα μεταδεδομένα XMP. Το `DublinCorePackage` περιέχει τυπικά πεδία Dublin Core όπως τίτλος, δημιουργός και λέξεις‑κλειδιά.

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### Βήμα 8: Ενημέρωση Μεταδεδομένων XMP στην Εικόνα

Ενημερώστε τα μεταδεδομένα XMP στην εικόνα χρησιμοποιώντας τη μέθοδο `setXmpData`. Αυτή η κλήση γράφει το πακέτο XMP στην ενότητα μεταδεδομένων της εικόνας. Η `setXmpData` γράφει το πακέτο XMP στην ενότητα μεταδεδομένων της εικόνας.

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### Βήμα 9: Αποθήκευση της Εικόνας

Μπορείτε τώρα να αποθηκεύσετε την εικόνα με τα ενσωματωμένα μεταδεδομένα XMP στον δίσκο ή σε ροή μνήμης.

```java
    image.save(ms);
```

### Βήμα 10: Φόρτωση της Εικόνας και Ανάκτηση Μεταδεδομένων XMP

Για να ανακτήσετε τα μεταδεδομένα XMP από την εικόνα, φορτώστε την εικόνα από τη ροή μνήμης ή τον δίσκο και προσπελάστε τα δεδομένα XMP μέσω της μεθόδου `getXmpData`. Η `getXmpData` διαβάζει το ενσωματωμένο πακέτο XMP από την εικόνα.

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

Συγχαρητήρια! Έχετε μάθει με επιτυχία πώς να διαχειρίζεστε δεδομένα XMP σε εικόνες χρησιμοποιώντας το Aspose.Imaging για Java. Αυτό σας επιτρέπει να αποθηκεύετε και να ανακτάτε πολύτιμα μεταδεδομένα μέσα στα αρχεία εικόνας σας.

## Συχνά Προβλήματα και Λύσεις

- **Τα μεταδεδομένα δεν εμφανίζονται στο Photoshop:** Βεβαιωθείτε ότι το πακέτο XMP ακολουθεί το σωστό σχήμα XML· το Aspose.Imaging το επικυρώνει αυτόματα, αλλά οι προσαρμοσμένοι χώροι ονομάτων ενδέχεται να χρειάζονται καταχώριση.  
- **Τα μεγάλα αρχεία TIFF προκαλούν OutOfMemoryError:** Χρησιμοποιήστε `TiffOptions` με `Compression` ορισμένο σε `LZW` και ενεργοποιήστε τη ροή (`loadOptions.setBufferSize`) για να διατηρήσετε τη χρήση μνήμης χαμηλή.  
- **Απρόσμενη κωδικοποίηση χαρακτήρων:** Το XMP αναμένει UTF‑8· πάντα περάστε συμβολοσειρές χρησιμοποιώντας `StandardCharsets.UTF_8` για να αποφύγετε παραμορφωμένα δεδομένα.

## Συχνές Ερωτήσεις

**Q: Τι είναι τα μεταδεδομένα XMP;**  
A: Το XMP είναι ένα πρότυπο βασισμένο σε XML για ενσωμάτωση περιγραφικών πληροφοριών απευθείας σε αρχεία, επιτρέποντας συνεπή μεταδεδομένα μεταξύ εφαρμογών.

**Q: Γιατί είναι σημαντικά τα μεταδεδομένα XMP;**  
A: Σας επιτρέπει να ετικετοποιείτε τις εικόνες με συγγραφέα, πνευματικά δικαιώματα, λέξεις‑κλειδιά και προσαρμοσμένα δεδομένα, βελτιώνοντας την αναζητησιμότητα και τη διαχείριση περιουσιακών στοιχείων χωρίς εξωτερικές βάσεις δεδομένων.

**Q: Μπορώ να επεξεργαστώ τα μεταδεδομένα XMP μετά την ενσωμάτωσή τους σε μια εικόνα;**  
A: Ναι, το Aspose.Imaging για Java παρέχει μεθόδους για τροποποίηση υπαρχόντων πακέτων XMP και επαναγραφή τους στο αρχείο.

**Q: Είναι το Aspose.Imaging για Java δωρεάν εργαλείο;**  
A: Μια δωρεάν δοκιμή είναι διαθέσιμη για αξιολόγηση, αλλά απαιτείται πληρωμένη άδεια για παραγωγική χρήση. Μπορείτε να εξερευνήσετε επιλογές στην [Aspose.Imaging for Java website](https://purchase.aspose.com/buy).

**Q: Πού μπορώ να λάβω βοήθεια και υποστήριξη για το Aspose.Imaging για Java;**  
A: Επισκεφθείτε τα [Aspose.Imaging forums](https://forum.aspose.com/) για βοήθεια από την κοινότητα, ή επικοινωνήστε απευθείας με την υποστήριξη της Aspose για πελάτες με πληρωμένη άδεια.

## Συμπέρασμα

Σε αυτό το tutorial, εξετάσαμε πώς να εργαστούμε με μεταδεδομένα XMP σε εικόνες χρησιμοποιώντας το Aspose.Imaging για Java, μια κορυφαία **java image processing library**. Ακολουθώντας τον οδηγό βήμα‑βήμα, μπορείτε εύκολα να ενσωματώσετε, να ενημερώσετε και να ανακτήσετε δεδομένα XMP, εμπλουτίζοντας τα ψηφιακά σας περιουσιακά στοιχεία με αναζητήσιμα, πρότυπα‑συμβατά μεταδεδομένα.

---

**Τελευταία Ενημέρωση:** 2026-05-18  
**Δοκιμάστηκε Με:** Aspose.Imaging for Java 24.12  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Κατακτήστε την Επεξεργασία Εικόνας Java: Τροποποίηση Δεδομένων EXIF με Aspose.Imaging](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [Επεξεργασία Εικόνας Java με Aspose.Imaging: Φόρτωση, Βελτίωση & Αποθήκευση Εικόνων](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [Προχωρημένη Επεξεργασία Εικόνας Java με τη Βιβλιοθήκη Aspose.Imaging](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)


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
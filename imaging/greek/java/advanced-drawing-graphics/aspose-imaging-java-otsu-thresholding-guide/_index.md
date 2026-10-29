---
date: '2026-10-29'
description: Μάθετε πώς να μετατρέψετε την εικόνα σε δυαδική μορφή χρησιμοποιώντας
  Aspose.Imaging for Java με Otsu thresholding. Οδηγός step‑by‑step καλύπτει setup,
  caching και saving σε πολλαπλές μορφές εικόνας Java.
keywords:
- convert image to binary
- java image processing
- image thresholding otsu
- apply otsu threshold
- java image formats
- aspose imaging java
lastmod: '2026-10-29'
og_description: Μάθετε πώς να μετατρέψετε την εικόνα σε δυαδική μορφή χρησιμοποιώντας
  Aspose.Imaging for Java με Otsu thresholding. Οδηγός step‑by‑step καλύπτει setup,
  caching και saving σε πολλαπλές μορφές εικόνας Java.
og_image_alt: 'Guide: convert image to binary using Otsu thresholding in Java with
  Aspose.Imaging'
og_title: Πώς να μετατρέψετε την εικόνα σε δυαδική μορφή με Otsu thresholding σε Java
schemas:
- author: Aspose
  dateModified: '2026-10-29'
  description: Learn how to convert image to binary using Aspose.Imaging for Java
    with Otsu thresholding. Step‑by‑step guide covers setup, caching, and saving across
    multiple Java image formats.
  headline: How to convert image to binary with Otsu thresholding in Java
  type: TechArticle
- description: Learn how to convert image to binary using Aspose.Imaging for Java
    with Otsu thresholding. Step‑by‑step guide covers setup, caching, and saving across
    multiple Java image formats.
  name: How to convert image to binary with Otsu thresholding in Java
  steps:
  - name: '**Aspose.Imaging for Java** – the core library that powers all image operations.'
    text: '**Aspose.Imaging for Java** – the core library that powers all image operations.'
  - name: '**Java Development Kit (JDK)** – version 8 or higher.'
    text: '**Java Development Kit (JDK)** – version 8 or higher.'
  - name: '**Document analysis** – Pre‑process scanned pages before OCR (e.g., *aspose
      imaging ocr*).'
    text: '**Document analysis** – Pre‑process scanned pages before OCR (e.g., *aspose
      imaging ocr*).'
  - name: '**Medical imaging** – Clean up X‑ray or MRI slices for pattern detection.'
    text: '**Medical imaging** – Clean up X‑ray or MRI slices for pattern detection.'
  - name: '**Computer vision** – Provide binary inputs to machine‑learning models
      that expect black‑and‑white data.'
    text: '**Computer vision** – Provide binary inputs to machine‑learning models
      that expect black‑and‑white data.'
  type: HowTo
- questions:
  - answer: Otsu’s method is a statistical technique that automatically selects the
      optimal global threshold to separate foreground from background in a gray‑level
      image.
    question: What is Otsu thresholding?
  - answer: Download the latest JAR from the [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/)
      page and add it to your project’s classpath.
    question: How do I set up Aspose.Imaging if I don’t use Maven or Gradle?
  - answer: Yes, the library supports PNG, BMP, GIF, TIFF, and many more formats.
    question: Can I process images other than JPEGs with Aspose.Imaging?
  - answer: Caching stores pixel data in RAM, dramatically speeding up repeated operations
      such as filtering or binarization—often by a factor of two to three.
    question: What are the benefits of caching RasterImages?
  - answer: Visit [Aspose's purchase page](https://purchase.aspose.com/buy) to explore
      licensing options and complete your acquisition.
    question: How do I purchase a license for Aspose.Imaging?
  type: FAQPage
tags:
- convert image to binary
- Aspose.Imaging
- Java image processing
- Otsu thresholding
- binary image conversion
title: Πώς να μετατρέψετε την εικόνα σε δυαδική μορφή με Otsu thresholding σε Java
url: /el/java/advanced-drawing-graphics/aspose-imaging-java-otsu-thresholding-guide/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αρχική επεξεργασία εικόνας σε Java: ένας λεπτομερής οδηγός για το Aspose.Imaging για Java

## Εισαγωγή

Αν χρειάζεστε **μετατροπή εικόνας σε δυαδική μορφή** αποδοτικά για αναλύσεις, αποθήκευση ή pipelines μηχανικής μάθησης, βρίσκεστε στο σωστό μέρος. Η μετατροπή μιας έγχρωμης ή γκρι κλίμακας εικόνας σε καθαρή ασπρόμαυρη μπορεί να μειώσει το μέγεθος του αρχείου έως και 90 % και να κάνει τις επόμενες εργασίες OCR ή υπολογιστικής όρασης πολύ πιο απλές. Αυτό το σεμινάριο σας καθοδηγεί στη χρήση του **Aspose.Imaging for Java** για φόρτωση, προσωρινή αποθήκευση, εφαρμογή του κατωφλίου Otsu και τελικά **αποθήκευση επεξεργασμένων εικόνων** — όλα ενώ διατηρείτε τον κώδικά σας καθαρό και αποδοτικό. Θα κατανοήσετε επίσης γιατί κάθε βήμα είναι σημαντικό, ώστε να προσαρμόσετε την προσέγγιση σε οποιοδήποτε έργο επεξεργασίας εικόνας σε Java.

## Γρήγορες απαντήσεις
- **Τι σημαίνει η “μετατροπή εικόνας σε δυαδική μορφή”;** Σημαίνει ότι κάθε pixel μετατρέπεται σε μαύρο ή λευκό βάσει ενός υπολογισμένου κατωφλίου, παράγοντας μια πραγματικά δυαδική εικόνα.  
- **Ποιος αλγόριθμος χρησιμοποιείται σε αυτόν τον οδηγό;** Η παγκόσμια μέθοδος κατωφλίου του Otsu, η οποία επιλέγει αυτόματα το βέλτιστο όριο για ολόκληρη την εικόνα.  
- **Χρειάζομαι άδεια για να το δοκιμάσω;** Μια δωρεάν δοκιμή ή προσωρινή άδεια σας επιτρέπει να αξιολογήσετε όλες τις λειτουργίες χωρίς κόστος.  
- **Μπορώ να επεξεργαστώ μορφές εκτός του JPEG;** Ναι — το Aspose.Imaging υποστηρίζει PNG, BMP, TIFF, GIF και περισσότερα από 150 μορφές εικόνας.  
- **Ποια έκδοση Java απαιτείται;** JDK 8 ή νεότερη.

## Τι είναι η μετατροπή εικόνας σε δυαδική μορφή;
**Η μετατροπή εικόνας σε δυαδική μορφή** είναι η διαδικασία μετατροπής μιας εικόνας γκρι κλίμακας σε ασπρόμαυρη εικόνα όπου κάθε pixel είναι είτε 0 (μαύρο) είτε 255 (λευκό) βάσει μιας τιμής κατωφλίου. Αυτή η μετατροπή αφαιρεί τις πληροφορίες χρώματος, απλοποιώντας δραστικά την ανάλυση για OCR, αναγνώριση προτύπων και πολλούς αλγόριθμούς υπολογιστικής όρασης.

## Γιατί να χρησιμοποιήσετε το Aspose.Imaging για Java;
Το Aspose.Imaging υποστηρίζει **πάνω από 150 μορφές εισόδου και εξόδου** — συμπεριλαμβανομένων PNG, BMP, TIFF, GIF και JPEG — ενώ επεξεργάζεται έγγραφα με εκατοντάδες σελίδες χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη. Ο ενσωματωμένος αλγόριθμος Otsu εξαλείφει την ανάγκη για προσαρμοσμένο κώδικα κατωφλίου, και οι μηχανισμοί προσωρινής αποθήκευσης της βιβλιοθήκης βελτιώνουν τη ροή εργασίας σε σενάρια παρτίδας. Το προϊόν προσφέρει επίσης απλή άδεια: ξεκινήστε με δωρεάν δοκιμή, προχωρήστε σε προσωρινή άδεια για μεγαλύτερη αξιολόγηση ή αγοράστε πλήρη άδεια για παραγωγική χρήση.

## Προαπαιτούμενα

### Απαιτούμενες βιβλιοθήκες και εκδόσεις
1. **Aspose.Imaging for Java** – η βασική βιβλιοθήκη που τροφοδοτεί όλες τις λειτουργίες εικόνας.  
2. **Java Development Kit (JDK)** – έκδοση 8 ή νεότερη.

### Απαιτήσεις ρύθμισης περιβάλλοντος
- Ένα IDE όπως IntelliJ IDEA, Eclipse ή NetBeans.  
- Maven ή Gradle για διαχείριση εξαρτήσεων.

### Προαπαιτούμενες γνώσεις
- Βασική εξοικείωση με τη σύνταξη της Java.  
- Γενική κατανόηση των εννοιών επεξεργασίας εικόνας (pixels, γκρι κλίμακα, κατώφλια).

## Ρύθμιση του Aspose.Imaging για Java

Πριν ξεκινήσετε τον κώδικα, προσθέστε τη βιβλιοθήκη στο έργο σας.

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

**Direct download:**  
Αποκτήστε πρόσβαση στα [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) για να κατεβάσετε τη βιβλιοθήκη απευθείας.

### Βήματα απόκτησης άδειας
- **Δωρεάν δοκιμή** – εξερευνήστε όλες τις λειτουργίες χωρίς κόστος.  
- **Προσωρινή άδεια** – επεκτείνετε την περίοδο δοκιμής για μεγαλύτερα έργα.  
- **Αγορά** – αποκτήστε πλήρη άδεια από το [Aspose](https://purchase.aspose.com/buy).

Για να ξεκινήσετε, δημιουργήστε μια παρουσία `Image` και φορτώστε ένα αρχείο:

Η κλάση `Image` αντιπροσωπεύει μια εικόνα και παρέχει μεθόδους για φόρτωση και διαχείριση δεδομένων εικόνας.  
```java
import com.aspose.imaging.Image;

String dataDir = "YOUR_DOCUMENT_DIRECTORY";
try (Image image = Image.load(dataDir + "/aspose-logo.jpg")) {
    // Image loaded successfully
}
```

## Οδηγός υλοποίησης

### Χαρακτηριστικό 1: φόρτωση εικόνας και αρχικοποίηση

#### Επισκόπηση
Η φόρτωση του αρχείου προέλευσης είναι το πρώτο βήμα σε οποιαδήποτε ροή εργασίας **java image processing**.

#### Άμεση απάντηση
Φορτώστε την εικόνα προέλευσης με `Image.load(dataDir + "sample.jpg")`; αυτό δημιουργεί μια αναπαράσταση στη μνήμη που μπορείτε να χειριστείτε με το API του Aspose.Imaging.

**Load an Image**  
```java
import com.aspose.imaging.Image;

String dataDir = "YOUR_DOCUMENT_DIRECTORY";
try (Image image = Image.load(dataDir + "/aspose-logo.jpg")) {
    // The image is now loaded and ready for further manipulation.
}
```

Βεβαιωθείτε ότι το `dataDir` δείχνει στο φάκελο που περιέχει την εικόνα προέλευσης.

### Χαρακτηριστικό 2: προσωρινή αποθήκευση rasterImage

#### Επισκόπηση
Η προσωρινή αποθήκευση αποθηκεύει τα δεδομένα pixel στη μνήμη, κάτι που **βελτιστοποιεί την επεξεργασία εικόνας** όταν εκτελείτε πολλαπλές λειτουργίες στην ίδια εικόνα.

#### Άμεση απάντηση
Καλέστε `RasterCachedImage.cacheData()` μετά τη φόρτωση· αυτό αποθηκεύει τα raster δεδομένα ώστε οι επόμενες λειτουργίες όπως φιλτράρισμα ή δυαδικοποίηση να εκτελούνται πιο γρήγορα.

Η κλάση `RasterCachedImage` παρέχει δυνατότητες προσωρινής αποθήκευσης για raster εικόνες, και η μέθοδος `cacheData()` της αποθηκεύει τα δεδομένα pixel στη μνήμη.  
**Cache Image Data**  
```java
import com.aspose.imaging.RasterCachedImage;

// Assume 'image' is an instance of Image that has been loaded previously
RasterCachedImage rasterCachedImage = (RasterCachedImage) image;
if (!rasterCachedImage.isCached()) {
    // Cache the image data if it's not already cached
    rasterCachedImage.cacheData();
}
```

### Χαρακτηριστικό 3: δυαδικοποίηση με κατώφλι Otsu

#### Επισκόπηση
Αυτό το βήμα εκτελεί τη **μετατροπή εικόνας σε δυαδική μορφή** που χρειάζεστε για OCR, αναγνώριση προτύπων ή ανάλυση εγγράφων.

#### Άμεση απάντηση
Κληθείτε `image.binarizeOtsu()` στο προσωρινά αποθηκευμένο raster· η μέθοδος υπολογίζει αυτόματα το βέλτιστο παγκόσμιο κατώφλι χρησιμοποιώντας τον αλγόριθμο Otsu και επιστρέφει μια καθαρή ασπρόμαυρη εικόνα.

Η μέθοδος `binarizeOtsu()` ενός αντικειμένου `Image` εφαρμόζει τον αλγόριθμο Otsu για να παραγάγει μια δυαδική εικόνα.  
**Apply Otsu's method**  
```java
// Assume 'rasterCachedImage' is an instance of RasterCachedImage that has been cached previously
class FeatureBinarizationWithOtsuThreshold {
    // Binarize the image using Otsu Thresholding method
    rasterCachedImage.binarizeOtsu();
}
```

### Χαρακτηριστικό 4: αποθήκευση επεξεργασμένης εικόνας

#### Επισκόπηση
Μετά τη δυαδικοποίηση, θα θέλετε να **αποθηκεύσετε επεξεργασμένες εικόνες** για μελλοντική χρήση ή διανομή.

#### Άμεση απάντηση
Χρησιμοποιήστε `image.save(outputPath, new JpegOptions())` (ή άλλες επιλογές μορφής) για να γράψετε τη δυαδική εικόνα στο δίσκο· μπορείτε να αλλάξετε την επέκταση αρχείου και τις επιλογές ώστε να ταιριάζουν σε PNG, BMP ή TIFF εξόδους.

Η μέθοδος `save` γράφει την εικόνα στο δίσκο χρησιμοποιώντας τις καθορισμένες επιλογές μορφής, όπως `JpegOptions`.  
**Save the image**  
```java
import com.aspose.imaging.imageoptions.JpegOptions;

String outputDir = "YOUR_OUTPUT_DIRECTORY";
// Assume 'rasterCachedImage' is an instance of RasterCachedImage that has been processed previously
class FeatureSaveProcessedImage {
    rasterCachedImage.save(outputDir + "/BinarizationWithOtsuThreshold_out.jpg");
}
```

## Πρακτικές εφαρμογές

1. **Ανάλυση εγγράφων** – Προεπεξεργασία σαρωμένων σελίδων πριν το OCR (π.χ., *aspose imaging ocr*).  
2. **Ιατρική απεικόνιση** – Καθαρισμός τομών X‑ray ή MRI για ανίχνευση προτύπων.  
3. **Υπολογιστική όραση** – Παροχή δυαδικών εισόδων σε μοντέλα μηχανικής μάθησης που απαιτούν ασπρόμαυρα δεδομένα.

## Σκέψεις απόδοσης

- **Διαχείριση μνήμης** – Κάντε προσωρινή αποθήκευση μόνο των εικόνων που χρειάζεστε· απελευθερώστε πόρους με try‑with‑resources.  
- **Επεξεργασία παρτίδας** – Επανάληψη σε φάκελο αρχείων για μείωση του κόστους· το Aspose.Imaging μπορεί να επεξεργαστεί παρτίδες 500 MB σε λιγότερο από 30 δευτερόλεπτα σε τυπικό διακομιστή.  
- **Καθαρισμός πόρων** – Πάντα κλείστε τα ρεύματα εικόνας για να αποφύγετε διαρροές μνήμης.

## Συχνά προβλήματα και λύσεις

| Σύμπτωμα | Πιθανή αιτία | Διόρθωση |
|----------|--------------|----------|
| `OutOfMemoryError` κατά την επεξεργασία μεγάλων αρχείων | Η εικόνα δεν έχει προσωρινά αποθηκευτεί ή είναι ανοιχτές πολλές εικόνες | Χρησιμοποιήστε `RasterCachedImage.cacheData()` και κλείστε κάθε εικόνα σε μπλοκ `try‑with‑resources`. |
| Το δυαδικό αποτέλεσμα φαίνεται πολύ σκοτεινό | Λανθασμένος χρωματικός χώρος εικόνας | Βεβαιωθείτε ότι η εικόνα προέλευσης είναι γκρι κλίμακας πριν καλέσετε `binarizeOtsu()`. |
| Το μέγεθος του αποθηκευμένου αρχείου είναι μεγαλύτερο από το αναμενόμενο | Χρήση JPEG με υψηλή ποιότητα | Ρυθμίστε την ποιότητα στο `JpegOptions` ή μεταβείτε σε PNG για αποθήκευση χωρίς απώλειες. |

## Συχνές ερωτήσεις

**Ε: Τι είναι η κατωφλίωση Otsu;**  
Η μέθοδος του Otsu είναι μια στατιστική τεχνική που επιλέγει αυτόματα το βέλτιστο παγκόσμιο κατώφλι για να διαχωρίσει το προσκήνιο από το φόντο σε μια εικόνα γκρι επιπέδου.

**Ε: Πώς ρυθμίζω το Aspose.Imaging αν δεν χρησιμοποιώ Maven ή Gradle;**  
Κατεβάστε το πιο πρόσφατο JAR από τη σελίδα [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) και προσθέστε το στο classpath του έργου σας.

**Ε: Μπορώ να επεξεργαστώ εικόνες εκτός των JPEG με το Aspose.Imaging;**  
Ναι, η βιβλιοθήκη υποστηρίζει PNG, BMP, GIF, TIFF και πολλές άλλες μορφές.

**Ε: Ποια είναι τα οφέλη της προσωρινής αποθήκευσης RasterImages;**  
Η προσωρινή αποθήκευση αποθηκεύει τα δεδομένα pixel στη RAM, επιταχύνοντας δραστικά τις επαναλαμβανόμενες λειτουργίες όπως φιλτράρισμα ή δυαδικοποίηση — συχνά κατά έναν ή δύο έως τρεις παράγοντες.

**Ε: Πώς αγοράζω άδεια για το Aspose.Imaging;**  
Επισκεφθείτε τη [σελίδα αγοράς του Aspose](https://purchase.aspose.com/buy) για να εξερευνήσετε τις επιλογές αδειοδότησης και να ολοκληρώσετε την απόκτηση.

## Πόροι

- **Τεκμηρίωση**: Εξερευνήστε όλες τις δυνατότητες στο [Aspose.Imaging Java Documentation](https://reference.aspose.com/imaging/java/).  
- **Λήψη**: Λάβετε την πιο πρόσφατη έκδοση της βιβλιοθήκης από τα [Aspose releases](https://releases.aspose.com/imaging/java/).  
- **Αγορά**: Μάθετε περισσότερα για τις επιλογές αδειοδότησης στη [σελίδα αγοράς του Aspose](https://purchase.aspose.com/buy).  
- **Δωρεάν δοκιμή & προσωρινή άδεια**: Δοκιμάστε το Aspose.Imaging με δωρεάν δοκιμή ή ζητήστε προσωρινή άδεια στο [Aspose Licensing](https://purchase.aspose.com/temporary-license/).  
- **Υποστήριξη**: Κάντε ερωτήσεις στο [Aspose support forum](https://forum.aspose.com/c/imaging/14).

---

**Τελευταία ενημέρωση:** 2026-10-29  
**Δοκιμάστηκε με:** Aspose.Imaging 25.5 for Java  
**Συγγραφέας:** Aspose

## Σχετικά μαθήματα

- [Πλήρης Οδηγός: Aspose.Imaging Java για Επεξεργασία & Εξαγωγή Εικόνας](/imaging/java/getting-started/aspose-imaging-java-image-processing-guide/)
- [Φίλτρο Κίνησης Wiener σε Java με Aspose.Imaging: Οδηγός Επεξεργασίας Εικόνας](/imaging/java/image-filtering-effects/java-image-processing-motion-wiener-filter-aspose-imaging/)
- [Επεξεργασία PNG σε Java με Aspose.Imaging: Ένας Πλήρης Οδηγός](/imaging/java/format-specific-operations/mastering-png-processing-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
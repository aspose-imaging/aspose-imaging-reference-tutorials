---
date: '2026-07-27'
description: Μάθετε πώς να συμπιέσετε JPEG σε Java χρησιμοποιώντας το Aspose.Imaging.
  Εξερευνήστε την image processing σε Java, τις jpeg quality settings και τις optimization
  techniques για αποτελέσματα υψηλής ποιότητας.
keywords:
- Aspose.Imaging Java
- JPEG processing in Java
- Java image manipulation
- load and save JPEG with Aspose.Imaging
- format-specific operations
lastmod: '2026-07-27'
og_description: Μάθετε πώς να συμπιέσετε JPEG σε Java χρησιμοποιώντας το Aspose.Imaging.
  Αυτός ο οδηγός καλύπτει την java image processing, τις jpeg quality settings και
  την optimization για ταχύτερη απόδοση στο web.
og_image_alt: 'Developer guide: Compress JPEG in Java using Aspose.Imaging'
og_title: Πώς να Συμπιέσετε JPEG σε Java με τη Βιβλιοθήκη Aspose.Imaging
schemas:
- author: Aspose
  dateModified: '2026-07-27'
  description: Learn how to compress JPEG in Java using Aspose.Imaging. Explore java
    image processing, jpeg quality settings, and optimization techniques for high‑quality
    results.
  headline: How to Compress JPEG in Java with Aspose.Imaging Library
  type: TechArticle
- description: Learn how to compress JPEG in Java using Aspose.Imaging. Explore java
    image processing, jpeg quality settings, and optimization techniques for high‑quality
    results.
  name: How to Compress JPEG in Java with Aspose.Imaging Library
  steps:
  - name: '**Photography Apps:** Convert and save images in different formats to enhance
      visual appeal.'
    text: '**Photography Apps:** Convert and save images in different formats to enhance
      visual appeal.'
  - name: '**Web Development:** Optimize JPEGs for faster page loads with appropriate
      color modes and quality settings.'
    text: '**Web Development:** Optimize JPEGs for faster page loads with appropriate
      color modes and quality settings.'
  - name: '**Digital Archiving:** Maintain high‑quality image archives by choosing
      suitable compression settings.'
    text: '**Digital Archiving:** Maintain high‑quality image archives by choosing
      suitable compression settings.'
  - name: '**Print Media Production:** Use CMYK mode for printing‑ready images, ensuring
      accurate color reproduction.'
    text: '**Print Media Production:** Use CMYK mode for printing‑ready images, ensuring
      accurate color reproduction.'
  - name: '**Image Editing Software:** Allow users to preview and save images in multiple
      formats, leveraging Aspose.Imaging''s batch capabilities.'
    text: '**Image Editing Software:** Allow users to preview and save images in multiple
      formats, leveraging Aspose.Imaging''s batch capabilities.'
  type: HowTo
- questions:
  - answer: A quality setting of **75‑85** provides a good trade‑off between visual
      quality and file size for most browsers.
    question: What is the recommended JPEG quality value for web images?
  - answer: Yes, set `JpegOptions.Progressive = true` to enable progressive encoding,
      which improves perceived load speed on slow connections.
    question: Can Aspose.Imaging handle progressive JPEGs?
  - answer: Load the PNG with `Image.load`, configure `JpegOptions` (including `Quality`),
      and call `save` with a `.jpg` extension.
    question: How do I convert a PNG to a compressed JPEG in one step?
  - answer: No hard limit, but you should monitor JVM heap usage and dispose of each
      `Image` after saving to avoid out‑of‑memory errors.
    question: Is there a limit to the number of images I can process in a batch?
  - answer: Starting with version 25.5, Aspose.Imaging includes experimental support
      for JPEG‑XL, enabling even better compression ratios.
    question: Does the library support JPEG‑XL or other next‑gen formats?
  type: FAQPage
tags:
- jpeg compression
- java image processing
- aspose imaging jpeg
- jpeg quality settings
- java image optimization
title: Πώς να Συμπιέσετε JPEG σε Java με τη Βιβλιοθήκη Aspose.Imaging
url: /el/java/format-specific-operations/aspose-imaging-java-jpeg-processing/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Κατακτώντας την Επεξεργασία Εικόνων με Aspose.Imaging Java: Φόρτωση και Αποθήκευση JPEG

## Εισαγωγή

Στον σημερινό ψηφιακό κόσμο, η διαχείριση της ποιότητας των εικόνων είναι κρίσιμη για προγραμματιστές που εργάζονται σε διάφορους κλάδους όπως η φωτογραφία, η παραγωγή μέσων και η ανάπτυξη λογισμικού. Εάν ψάχνετε να **how to compress JPEG** αποδοτικά στις εφαρμογές Java, αυτό το tutorial είναι ιδανικό για εσάς. Θα σας καθοδηγήσουμε στη διαδικασία αξιοποίησης των ισχυρών δυνατοτήτων του Aspose.Imaging για τη διαχείριση αρχείων JPEG, τον έλεγχο των ρυθμίσεων ποιότητας JPEG και την επίτευξη βέλτιστων αποτελεσμάτων βελτιστοποίησης εικόνας Java. Ας εμβαθύνουμε στις προαπαιτούμενες απαιτήσεις για να ξεκινήσετε!

## Γρήγορες Απαντήσεις
Η μέθοδος `Image.load` διαβάζει ένα αρχείο εικόνας στη μνήμη, ενώ το `JpegOptions` ρυθμίζει τις ρυθμίσεις εξόδου JPEG όπως η ποιότητα και ο τρόπος χρώματος.  

- **Ποιος είναι ο πιο απλός τρόπος για να συμπιέσετε ένα JPEG σε Java;** Φορτώστε την εικόνα με `Image.load`, ορίστε `JpegOptions.Quality` (0‑100), και στη συνέχεια καλέστε `save` με αυτές τις επιλογές.  
- **Ποια έκδοση του Aspose.Imaging υποστηρίζει τα πιο πρόσφατα πρότυπα JPEG;** Η έκδοση 25.5 και μεταγενέστερες περιλαμβάνουν πλήρη υποστήριξη JPEG‑XL και progressive JPEG.  
- **Χρειάζομαι άδεια για να συμπιέσω JPEGs σε παραγωγή;** Ναι, μια επί πληρωμή άδεια Aspose.Imaging αφαιρεί τα όρια αξιολόγησης και ενεργοποιεί επεξεργασία παρτίδας υψηλής απόδοσης.  
- **Μπορώ να επεξεργαστώ χιλιάδες εικόνες χωρίς να εξαντλήσω τη μνήμη;** Χρησιμοποιήστε `Image.dispose()` μετά από κάθε αποθήκευση και σκεφτείτε τις streaming APIs για μεγάλες παρτίδες.  
- **Ποιες δευτερεύουσες ρυθμίσεις επηρεάζουν το μέγεθος του JPEG;** Τα bits ανά κανάλι, η υποδειγματοληψία και ο τρόπος χρώματος (π.χ., Grayscale vs. CMYK) επηρεάζουν όλα το τελικό μέγεθος του αρχείου.

## Τι είναι η συμπίεση JPEG σε Java;
Η κλάση `JpegOptions` σας επιτρέπει να καθορίσετε παραμέτρους κωδικοποίησης JPEG όπως η ποιότητα, η υποδειγματοληψία και ο τύπος χρώματος.  
Η συμπίεση JPEG είναι ένας αλγόριθμος με απώλειες που μειώνει το μέγεθος του αρχείου απορρίπτοντας οπτικές πληροφορίες που το ανθρώπινο μάτι είναι λιγότερο πιθανό να παρατηρήσει. Στο Aspose.Imaging, ελέγχετε τη συμπίεση μέσω της κλάσης `JpegOptions`, όπου η ιδιότητα `Quality` (0‑100) αντιστοιχεί άμεσα στην ποσότητα των δεδομένων που διατηρούνται. Υψηλότερες τιμές ποιότητας διατηρούν περισσότερες λεπτομέρειες αλλά παράγουν μεγαλύτερα αρχεία, ενώ χαμηλότερες τιμές μειώνουν το μέγεθος με κόστος την οπτική πιστότητα.

## Γιατί να χρησιμοποιήσετε Aspose.Imaging για τη συμπίεση JPEG;
Το Aspose.Imaging υποστηρίζει **150+ image formats** και μπορεί να επεξεργαστεί έγγραφα πολλών εκατοντάδων σελίδων χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, παρέχοντας έως και **3× faster throughput** σε σύγκριση με τις εγγενείς βιβλιοθήκες Java. Το API του προσφέρει λεπτομερή έλεγχο των τρόπων χρώματος, των bits ανά κανάλι και της προοδευτικής κωδικοποίησης, καθιστώντας το την προτιμώμενη λύση για java image processing και jpeg quality settings.

## Προαπαιτούμενα

- **Απαιτούμενες Βιβλιοθήκες:** Βιβλιοθήκη Aspose.Imaging έκδοση **25.5** ή νεότερη (η βιβλιοθήκη υποστηρίζει JPEG‑XL, progressive JPEG και χρωματικούς χώρους CMYK).  
- **Ρύθμιση Περιβάλλοντος:** Ένα Java Development Kit (JDK) εγκατεστημένο και ρυθμισμένο στον υπολογιστή σας.  
- **Προαπαιτούμενες Γνώσεις:** Βασική κατανόηση του προγραμματισμού Java και των εννοιών αρχείων εικόνας.  

## Ρύθμιση Aspose.Imaging για Java

Για να ενσωματώσετε το Aspose.Imaging στο έργο σας, μπορείτε να χρησιμοποιήσετε είτε Maven είτε Gradle, ή να κατεβάσετε απευθείας τη βιβλιοθήκη. Ακολουθεί η διαδικασία για κάθε μέθοδο:

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

**Direct Download:**  
Μπορείτε να κατεβάσετε την πιο πρόσφατη έκδοση από [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### Απόκτηση Άδειας

Για να δοκιμάσετε το Aspose.Imaging, μπορείτε να ξεκινήσετε με μια δωρεάν δοκιμή ή να ζητήσετε προσωρινή άδεια. Εάν το έργο σας απαιτεί μακροπρόθεσμη χρήση, σκεφτείτε την αγορά πλήρους άδειας. Επισκεφθείτε [Purchase Aspose](https://purchase.aspose.com/buy) για περισσότερες πληροφορίες.

Μόλις ρυθμιστεί, η αρχικοποίηση και η διαμόρφωση της βιβλιοθήκης είναι απλή, θέτοντας τη βάση για απρόσκοπτες δυνατότητες επεξεργασίας εικόνας σε εφαρμογές Java.

## Οδηγός Υλοποίησης

Αυτή η ενότητα θα αναλύσει κάθε χαρακτηριστικό της φόρτωσης και αποθήκευσης εικόνων JPEG με συγκεκριμένους τρόπους χρώματος χρησιμοποιώντας το Aspose.Imaging.

### Χαρακτηριστικό 1: Φόρτωση και Αποθήκευση Εικόνας με Συγκεκριμένες Επιλογές JPEG

#### Επισκόπηση
Αυτό το χαρακτηριστικό δείχνει πώς να φορτώσετε μια εικόνα JPEG από το σύστημά σας, να διαμορφώσετε τις ιδιότητές της και να την αποθηκεύσετε με καθορισμένες επιλογές όπως bits ανά κανάλι και μετατροπή σε grayscale.

##### Βήμα-Βήμα Υλοποίηση:

**Βήμα 1: Ρύθμιση Καταλόγων**  
Ορίστε διαδρομές για τις πηγαίες εικόνες και τους φακέλους εξόδου.  
```java
String srcDir = "YOUR_DOCUMENT_DIRECTORY";
String outputFolder = "YOUR_OUTPUT_DIRECTORY";
```  

**Βήμα 2: Διαμόρφωση Επιλογών JPEG**  
Δημιουργήστε ένα αντικείμενο `JpegOptions` για να ορίσετε bits ανά κανάλι, ποιότητα και άλλες ρυθμίσεις.  
```java
JpegOptions options = new JpegOptions();
options.setBitsPerChannel((byte) 12); // Set bits per channel to 12
```  

**Βήμα 3: Φόρτωση και Αποθήκευση της Εικόνας**  
Η κλάση `Image` αντιπροσωπεύει μια εικόνα που έχει φορτωθεί στη μνήμη· χρησιμοποιήστε τη μέθοδο `load` για να διαβάσετε αρχεία. Φορτώστε μια εικόνα από τον φάκελό σας, εφαρμόστε τις ρυθμίσεις χρώματος και αποθηκεύστε την με τις καθορισμένες επιλογές JPEG.  
```java
Image image = Image.load(srcDir + "Rgb.jpg");
try {
    String outputPath = outputFolder + "/grayscale_12-bit.jpg";
    options.setColorType(JpegCompressionColorMode.Grayscale); // Set to grayscale
    image.save(outputPath, options);
} finally {
    image.dispose();  // Release resources after processing
}
```  

Αυτή η προσέγγιση σας επιτρέπει να προσαρμόσετε τον τρόπο αποθήκευσης των εικόνων, βελτιστοποιώντας την ποιότητα και το μέγεθος του αρχείου.

### Χαρακτηριστικό 2: Επανάληψη και Μετατροπή Εικόνων με Διαφορετικούς Τρόπους Χρώματος

#### Επισκόπηση
Εξερευνήστε διάφορους τρόπους χρώματος JPEG εφαρμόζοντας κάθε τρόπο στην ίδια εικόνα και αποθηκεύοντάς τα, δείχνοντας την ευελιξία του Aspose.Imaging.

##### Βήμα-Βήμα Υλοποίηση:

**Βήμα 1: Ορισμός Τύπων Χρώματος**  
Δημιουργήστε έναν πίνακα με διαφορετικούς τύπους χρώματος που θέλετε να εφαρμόσετε.  
```java
int[] colorTypes = new int[]{
    JpegCompressionColorMode.Grayscale,
    JpegCompressionColorMode.YCbCr,
    JpegCompressionColorMode.Rgb,
    JpegCompressionColorMode.Cmyk,
    JpegCompressionColorMode.Ycck
};
```  

**Βήμα 2: Επανάληψη και Αποθήκευση**  
Επανάληψη πάνω στους τύπους χρώματος, εφαρμογή του καθενός στην εικόνα σας και αποθήκευση με μοναδικό όνομα.  
```java
JpegOptions options = new JpegOptions();
options.setBitsPerChannel((byte) 12); // Set bits per channel

for (int i = 0; i < colorTypes.length; ++i) {
    options.setColorType(colorTypes[i]); // Apply current color type
    String fileName = JpegCompressionColorMode.getName(JpegCompressionColorMode.class, colorTypes[i]) + "_12-bit.jpg";
    String outputPath = outputFolder + "/" + fileName;
    
    Image image = Image.load(srcDir + "Rgb.jpg");
    try {
        image.save(outputPath, options);  // Save with current settings
    } finally {
        image.dispose();  // Release resources for each iteration
    }
}
```  

Αυτό το χαρακτηριστικό είναι ιδιαίτερα χρήσιμο για πειραματισμό και επιλογή των βέλτιστων τρόπων χρώματος για διάφορες περιπτώσεις χρήσης.

## Πώς η συμπίεση JPEG επηρεάζει το μέγεθος του αρχείου;

Η συμπίεση ενός JPEG μειώνει το μέγεθος του αρχείου εφαρμόζοντας διακριτό συνημίτονο μετασχηματισμό (DCT) και κβαντισμό. Όσο χαμηλότερη είναι η τιμή `Quality` που ορίζετε στο `JpegOptions`, τόσο πιο επιθετικός είναι ο κβαντισμός, παράγοντας μικρότερα αρχεία αλλά ενδεχομένως ορατά artefacts. Για τις περισσότερες διαδικτυακές περιπτώσεις, μια ρύθμιση ποιότητας μεταξύ **70‑85** προσφέρει καλή ισορροπία μεταξύ οπτικής πιστότητας και εξοικονόμησης εύρους ζώνης.

## Πώς να επιλέξετε τον σωστό τρόπο χρώματος JPEG για συγκεκριμένη περίπτωση χρήσης;

Επιλέξτε τον τρόπο χρώματος με βάση το μέσο προορισμού:  
- **Grayscale** είναι ιδανικό για σάρωση εγγράφων και μειώνει το μέγεθος έως και **60 %** σε σύγκριση με πλήρες χρώμα.  
- **CMYK** απαιτείται για διαδικασίες εκτύπωσης, διατηρώντας δεδομένα χρώματος ειδικά για μελάνι.  
- **RGB** είναι η προεπιλογή για οθόνες και διαδικτυακή παράδοση. Προσαρμόστε το `JpegOptions.BitsPerChannel` ανάλογα (8 bits για τυπικό, 12 bits για σενάρια υψηλής δυναμικής περιοχής).

## Πρακτικές Εφαρμογές

1. **Εφαρμογές Φωτογραφίας:** Μετατροπή και αποθήκευση εικόνων σε διαφορετικές μορφές για βελτίωση της οπτικής ελκυστικότητας.  
2. **Ανάπτυξη Ιστού:** Βελτιστοποίηση JPEG για ταχύτερη φόρτωση σελίδων με κατάλληλους τρόπους χρώματος και ρυθμίσεις ποιότητας.  
3. **Ψηφιακή Αρχειοθέτηση:** Διατήρηση αρχείων υψηλής ποιότητας επιλέγοντας κατάλληλες ρυθμίσεις συμπίεσης.  
4. **Παραγωγή Εκτυπώσιμων Μέσων:** Χρήση τρόπου CMYK για εικόνες έτοιμες για εκτύπωση, εξασφαλίζοντας ακριβή αναπαραγωγή χρώματος.  
5. **Λογισμικό Επεξεργασίας Εικόνας:** Δυνατότητα στους χρήστες να προεπισκοπούν και να αποθηκεύουν εικόνες σε πολλαπλές μορφές, αξιοποιώντας τις δυνατότητες παρτίδας του Aspose.Imaging.

## Σκέψεις Απόδοσης

Για να εξασφαλίσετε ομαλή λειτουργία της εφαρμογής σας:

- **Βελτιστοποίηση Χρήσης Πόρων:** Πάντα απελευθερώνετε τα αντικείμενα `Image` μετά τη χρήση για ελευθέρωση μνήμης (`Image.dispose()`).  
- **Επεξεργασία Παρτίδας:** Επεξεργαστείτε πολλαπλές εικόνες παράλληλα εφόσον είναι δυνατόν, μειώνοντας το συνολικό χρόνο εκτέλεσης.  
- **Διαχείριση Μνήμης:** Παρακολουθείτε τη χρήση μνήμης της εφαρμογής και προσαρμόζετε τις ρυθμίσεις του Java Virtual Machine (JVM) όπως απαιτείται.  
- **Streaming API:** Για πολύ μεγάλες εικόνες JPEG, χρησιμοποιήστε `Image.load` με ροή (stream) για να αποφύγετε τη φόρτωση ολόκληρου του αρχείου στη μνήμη.

## Συχνά Προβλήματα και Λύσεις

- **Missing Output Directory:** Βεβαιωθείτε ότι ο φάκελος προορισμού υπάρχει πριν καλέσετε `save`; διαφορετικά θα προκληθεί `IOException`.  
- **License Restrictions:** Σε λειτουργία αξιολόγησης, το Aspose.Imaging περιορίζει τον αριθμό των σελίδων που επεξεργάζονται· αποκτήστε άδεια για απεριόριστη χρήση.  
- **Color Shift After Conversion:** Επαληθεύστε ότι το προφίλ χρώματος της πηγαίας εικόνας ταιριάζει με το επιθυμητό αποτέλεσμα (π.χ., sRGB vs. AdobeRGB) και ορίστε το `JpegOptions.ColorType` αναλόγως.

## Συχνές Ερωτήσεις

**Q: Ποια είναι η συνιστώμενη τιμή ποιότητας JPEG για εικόνες ιστού;**  
A: Μια ρύθμιση ποιότητας **75‑85** προσφέρει καλή ισορροπία μεταξύ οπτικής ποιότητας και μεγέθους αρχείου για τους περισσότερους browsers.

**Q: Μπορεί το Aspose.Imaging να διαχειριστεί progressive JPEGs;**  
A: Ναι, ορίστε `JpegOptions.Progressive = true` για ενεργοποίηση προοδευτικής κωδικοποίησης, η οποία βελτιώνει την αντιληπτική ταχύτητα φόρτωσης σε αργές συνδέσεις.

**Q: Πώς μετατρέπω ένα PNG σε συμπιεσμένο JPEG σε ένα βήμα;**  
A: Φορτώστε το PNG με `Image.load`, διαμορφώστε το `JpegOptions` (συμπεριλαμβανομένου του `Quality`) και καλέστε `save` με επέκταση `.jpg`.

**Q: Υπάρχει όριο στον αριθμό των εικόνων που μπορώ να επεξεργαστώ σε μια παρτίδα;**  
A: Δεν υπάρχει σκληρό όριο, αλλά θα πρέπει να παρακολουθείτε τη χρήση heap του JVM και να απελευθερώνετε κάθε `Image` μετά την αποθήκευση για να αποφύγετε σφάλματα out‑of‑memory.

**Q: Υποστηρίζει η βιβλιοθήκη JPEG‑XL ή άλλες επόμενες γενιές μορφών;**  
A: Από την έκδοση 25.5, το Aspose.Imaging περιλαμβάνει πειραματική υποστήριξη για JPEG‑XL, προσφέροντας ακόμη καλύτερους λόγους συμπίεσης.

## Συμπέρασμα

Με την κατάκτηση αυτών των τεχνικών, μπορείτε να βελτιώσετε σημαντικά τον τρόπο με τον οποίο οι εφαρμογές Java διαχειρίζονται εργασίες επεξεργασίας εικόνας. Είτε πρόκειται για βελτιστοποίηση ποιότητας, μείωση εύρους ζώνης ή προετοιμασία περιουσιακών στοιχείων για εκτύπωση, το Aspose.Imaging προσφέρει ισχυρές λύσεις για τη διαχείριση εικόνων JPEG με διάφορους τρόπους χρώματος και ρυθμίσεις συμπίεσης.

### Επόμενα Βήματα
- Πειραματιστείτε με άλλα χαρακτηριστικά της βιβλιοθήκης Aspose.Imaging, όπως υδατογράφημα και διαχείριση μεταδεδομένων.  
- Εξερευνήστε την επίσημη τεκμηρίωση για να μάθετε για προχωρημένες επιλογές όπως **subsampling** και ενσωμάτωση χρωματικού προφίλ.  
- Ενσωματώστε το πρότυπο επεξεργασίας παρτίδας στη CI/CD pipeline σας για αυτόματη βελτιστοποίηση εικόνων κατά το χρόνο κατασκευής.

Έτοιμοι να ανεβάσετε τις δεξιότητές σας στην επεξεργασία εικόνας στο επόμενο επίπεδο; Ξεκινήστε να εφαρμόζετε αυτές τις τεχνικές στα Java projects σας σήμερα!

## Πόροι

- **Documentation:** [Aspose.Imaging Java Documentation](https://reference.aspose.com/imaging/java/)  
- **Download:** [Aspose.Imaging for Java Releases](https://releases.aspose.com/imaging/java/)  
- **Purchase:** [Buy Aspose Licensing](https://purchase.aspose.com/buy)  
- **Free Trial:** [Aspose Imaging Free Trials](https://releases.aspose.com/imaging/java/)  
- **Temporary License:** [Request Temporary License](https://purchase.aspose.com/temporary-license/)  
- **Support:** [Aspose.Imaging Forum](https://forum.aspose.com/c/imaging/14)

---

**Last Updated:** 2026-07-27  
**Tested With:** Aspose.Imaging 25.5 for Java  
**Author:** Aspose

## Σχετικά Μαθήματα

- [Master Image Handling in Java with Aspose.Imaging: Load, Resize, Cache, and Save](/imaging/java/compression-optimization/efficient-image-handling-java-aspose-imaging/)
- [Efficient Image Processing in Java with Aspose.Imaging: Load, Filter, Save](/imaging/java/getting-started/master-image-processing-java-aspose-imaging/)
- [Aspose.Imaging Java: Load and Save WebP Image Frames Tutorial](/imaging/java/format-specific-operations/aspose-imaging-java-webp-frame-handling/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}
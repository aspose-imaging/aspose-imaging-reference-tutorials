---
date: '2026-09-28'
description: Μάθετε πώς να χρησιμοποιήσετε ccittfax3 compression java για να δημιουργήσετε
  αρχεία multi-page TIFF με Aspose.Imaging. Σαρώστε, αρχειοθετήστε και μειώστε αποδοτικά
  το μέγεθος των αρχείων για τις ροές εργασίας εγγράφων.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Ανακαλύψτε βήμα‑βήμα πώς να χρησιμοποιήσετε ccittfax3 compression
  java με Aspose.Imaging για να δημιουργήσετε αποδοτικά αρχεία multi‑page TIFF για
  σάρωση και αρχειοθέτηση.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: Πώς να δημιουργήσετε multi-page TIFF με ccittfax3 compression java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: Πώς να δημιουργήσετε multi-page TIFF με ccittfax3 compression java
url: /el/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Κατακτώντας τη δημιουργία πολυ-σελίδων TIFF με συμπίεση ccittfax3 java χρησιμοποιώντας το Aspose.Imaging

## Εισαγωγή

Αν χρειάζεστε να αρχειοθετήσετε μεγάλους όγκους σαρωμένων εγγράφων ενώ διατηρείτε μικρά τα μεγέθη των αρχείων, η **ccittfax3 compression java** είναι η προτιμώμενη λύση. Αυτό το σεμινάριο σας δείχνει πώς να δημιουργήσετε αρχεία TIFF πολλαπλών σελίδων με συμπίεση CCITTFAX3 σε Java χρησιμοποιώντας το Aspose.Imaging. Θα μάθετε γιατί αυτή η συμπίεση λειτουργεί τόσο καλά για μονόχρωμες σαρώσεις, πώς να διαμορφώσετε τη βιβλιοθήκη και πώς να προσθέσετε κάθε σελίδα ως καρέ.

**Τι θα μάθετε**
- Πώς να προσθέσετε το Aspose.Imaging σε ένα έργο Java.
- Πώς να διαμορφώσετε το `TiffOptions` για συμπίεση CCITTFAX3.
- Πώς να δημιουργήσετε ένα `TiffImage`, να αλλάξετε το μέγεθος των πηγαίων εικόνων και να τις προσθέσετε ως καρέ.
- Πώς να αποθηκεύσετε το τελικό πολυ‑σελίδων TIFF αποδοτικά.

Ας περάσουμε από την πλήρη υλοποίηση.

## Γρήγορες απαντήσεις
- **Ποιο είναι το κύριο όφελος της συμπίεσης CCITTFAX3;** Μείωση έως 80 % του μεγέθους του αρχείου για ασπρόμαυρες σαρώσεις.  
- **Ποια βιβλιοθήκη παρέχει ενσωματωμένη υποστήριξη;** Aspose.Imaging for Java, έκδοση 25.5+.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμαστική άδεια λειτουργεί για όλα τα χαρακτηριστικά· απαιτείται πληρωμένη άδεια για παραγωγή.  
- **Μπορώ να επεξεργαστώ εκατοντάδες σελίδες;** Ναι—το Aspose.Imaging μεταδίδει τις σελίδες, έτσι η χρήση μνήμης παραμένει χαμηλή.  
- **Είναι ο κώδικας συμβατός με Java 11 και νεότερες εκδόσεις;** Απόλυτα· το API στοχεύει σε Java 8+.

## Τι είναι η ccittfax3 compression java;
`CCITTFAX3` είναι ένας αλγόριθμος συμπίεσης χωρίς απώλειες, μονόχρωμος, σχεδιασμένος για fax και εικόνες σαρωμένων εγγράφων. Κωδικοποιεί κάθε pixel ως ένα μόνο bit, παρέχοντας υψηλής ποιότητας έξοδο ενώ μειώνει δραστικά το μέγεθος του αρχείου—συχνά κατά 70‑80 % σε σύγκριση με το μη συμπιεσμένο TIFF. Αυτό το καθιστά ιδανικό για αρχειοθέτηση ασπρόμαυρων εγγράφων όπου πρέπει να διατηρηθεί η πιστότητα.

## Γιατί να χρησιμοποιήσετε το Aspose.Imaging για αυτήν την εργασία;
Το Aspose.Imaging υποστηρίζει **100+** μορφές εισόδου και εξόδου, συμπεριλαμβανομένων των PDF, PNG, JPEG και TIFF. Η αρχιτεκτονική του με ροή μπορεί να διαχειριστεί **πολυ-εκατοντάδες‑σελίδες** αρχεία TIFF χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη, καθιστώντας το ιδανικό για έργα αρχειοθέτησης μεγάλης κλίμακας.

## Προαπαιτούμενα

- **Java Development Kit (JDK)** 8 ή νεότερο εγκατεστημένο.
- **IDE** όπως IntelliJ IDEA ή Eclipse.
- **Maven** ή **Gradle** για διαχείριση εξαρτήσεων.
- Βασικές γνώσεις Java (κλάσεις, αντικείμενα, συλλογές).

## Ρύθμιση του Aspose.Imaging για Java

Προσθέστε τη βιβλιοθήκη στο αρχείο κατασκευής σας.

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

### Άμεση λήψη

Μπορείτε επίσης να κατεβάσετε το τελευταίο JAR από [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### Απόκτηση άδειας

Μια δωρεάν δοκιμαστική άδεια είναι διαθέσιμη από τη [σελίδα Δωρεάν Δοκιμής του Aspose](https://releases.aspose.com/imaging/java/). Για παραγωγική χρήση, αγοράστε μόνιμη άδεια ή ζητήστε προσωρινή στο [Aspose Purchase](https://purchase.aspose.com/temporary-license/).

Για λεπτομερή χρήση του API, δείτε την [τεκμηρίωση](https://reference.aspose.com/imaging/java/) του Aspose.Imaging for Java.

### Βασική αρχικοποίηση

Αφού προσθέσετε την εξάρτηση, αρχικοποιήστε τη βιβλιοθήκη όπως φαίνεται παρακάτω.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## Πώς να διαμορφώσετε την ccittfax3 compression java για ένα πολυ‑σελίδων TIFF;

`TiffOptions` είναι μια κλάση που ορίζει τη μορφή εξόδου και τις ρυθμίσεις συμπίεσης για ένα αρχείο TIFF. Φορτώστε το αντικείμενο `TiffOptions` με την απαρίθμηση `CCITTGroup3FaxCompression`, στη συνέχεια ορίστε την πηγή του αρχείου εξόδου. Αυτή η διπλή διαμόρφωση προετοιμάζει τον γράφο για μονόχρωμη συμπίεση και εξασφαλίζει ότι κάθε σελίδα που θα προστεθεί αργότερα θα κωδικοποιηθεί χρησιμοποιώντας τον αλγόριθμο CCITTFAX3, με αποτέλεσμα σημαντική μείωση του μεγέθους ενώ διατηρείται η ποιότητα της εικόνας.

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## Πώς να δημιουργήσετε ένα αντικείμενο TiffImage σε Java;

`TiffImage` αντιπροσωπεύει ένα πολυ‑σελίδων έγγραφο TIFF στη μνήμη και παρέχει μεθόδους για τη διαχείριση των καρέ του. Πρώτα, ορίστε το πλάτος και το ύψος που θα μοιράζονται όλες οι σελίδες. Στη συνέχεια, δημιουργήστε ένα `TiffImage` χρησιμοποιώντας το προηγουμένως δημιουργημένο `TiffOptions`. Το αντικείμενο `TiffImage` λειτουργεί ως δοχείο για τα μεμονωμένα καρέ, επιτρέποντάς σας να προσθέτετε, να αφαιρείτε ή να αναδιατάσσετε σελίδες πριν αποθηκεύσετε το τελικό αρχείο.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## Πώς να φορτώσετε και να αλλάξετε το μέγεθος των πηγαίων εικόνων από φάκελο;

Φιλτράρετε τον προορισμό κατάλογο για αρχεία JPEG, διαβάστε κάθε εικόνα και αλλάξτε το μέγεθός της ώστε να ταιριάζει με τον καμβά του TIFF. Η αλλαγή μεγέθους πριν την προσθήκη των καρέ μειώνει την κατανάλωση μνήμης και επιταχύνει τη λειτουργία αποθήκευσης. Με τη μετατροπή κάθε πηγαίας εικόνας στις απαιτούμενες διαστάσεις και μορφή pixel, εξασφαλίζετε συνεπή διάταξη σελίδας και αποφεύγετε σφάλματα χρόνου εκτέλεσης όταν τα καρέ προσαρτώνται στο έγγραφο TIFF.

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## Πώς να προσθέσετε κάθε εικόνα ως καρέ στο πολυ‑σελίδων TIFF;

`TiffFrame` είναι ένα αντικείμενο που κρατά μια εικόνα μίας σελίδας και τα σχετιζόμενα μεταδεδομένα της μέσα σε ένα TIFF. Επανάλαβε τις αλλαγμένες εικόνες, δημιούργησε ένα νέο `TiffFrame` και πρόσθεσέ το στο `TiffImage`. Κάθε καρέ γίνεται ξεχωριστή σελίδα στο τελικό έγγραφο, και η βιβλιοθήκη χειρίζεται αυτόματα τις απαραίτητες ενημερώσεις μεταδεδομένων, όπως ο αριθμός σελίδων και οι μετατοπίσεις, εξασφαλίζοντας μια έγκυρη δομή πολυ‑σελίδων TIFF.

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## Πώς να αποθηκεύσετε το τελικό πολυ‑σελίδων αρχείο TIFF;

Καλέστε τη μέθοδο `save` στο αντικείμενο `TiffImage`, περνώντας τη ζητούμενη διαδρομή εξόδου. Η βιβλιοθήκη γράφει αυτόματα όλα τα καρέ χρησιμοποιώντας συμπίεση CCITTFAX3, μεταδίδει τα δεδομένα στο δίσκο αποδοτικά και κλείνει τυχόν υποκείμενους πόρους. Μετά την ολοκλήρωση της λειτουργίας αποθήκευσης, το προκύπτον αρχείο περιέχει όλες τις σελίδες με την καθορισμένη συμπίεση, έτοιμο για διανομή ή αρχειοθέτηση.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## Πρακτικές εφαρμογές

- **Αρχειοθέτηση εγγράφων:** Αποθηκεύστε σαρωμένες συμβάσεις, τιμολόγια ή νομικά αρχεία με ελάχιστο αποθηκευτικό κόστος.  
- **Ιατρική απεικόνιση:** Συμπιέστε σαρώσεις ακτινολογίας διατηρώντας τη διαγνωστική λεπτομέρεια.  
- **Παραγωγή εκτύπωσης:** Δημιουργήστε πολυ‑σελίδες εργασίες εκτύπωσης που οι εκτυπωτές μπορούν να καταναλώσουν άμεσα.

## Σκέψεις απόδοσης

- Χρησιμοποιήστε `ResizeOptions` που διατηρούν την αναλογία διαστάσεων για να αποφύγετε παραμόρφωση.  
- Κλείστε κάθε αντικείμενο `Image` μετά την προσθήκη του καρέ του για να ελευθερώσετε τη φυσική μνήμη.  
- Για πολύ μεγάλες παρτίδες, επεξεργαστείτε τα αρχεία σε παράλληλες ροές και γράψτε κάθε τμήμα TIFF ασύγχρονα.

## Συνηθισμένα προβλήματα και αντιμετώπιση

- **Λανθασμένη μορφή pixel:** Η CCITTFAX3 λειτουργεί μόνο με εικόνες 1‑bit (ασπρόμαυρες). Μετατρέψτε τις έγχρωμες εικόνες σε κλίμακα του γκρι πριν την αλλαγή μεγέθους.  
- **Διαρροές μνήμης:** Πάντα καλέστε `dispose()` σε προσωρινά αντικείμενα `Image`; διαφορετικά τα φυσικά buffers παραμένουν δεσμευμένα.  
- **Το μέγεθος του αρχείου δεν μειώνεται:** Βεβαιωθείτε ότι η ιδιότητα συμπίεσης του `TiffOptions` είναι ορισμένη· διαφορετικά χρησιμοποιείται η προεπιλογή (χωρίς συμπίεση).

## Συχνές ερωτήσεις

**Q: Μπορώ να χρησιμοποιήσω αυτήν την προσέγγιση με έγχρωμες εικόνες;**  
A: Η CCITTFAX3 περιορίζεται σε μονόχρωμα δεδομένα· για χρώμα χρησιμοποιήστε συμπίεση JPEG ή LZW.

**Q: Υποστηρίζει το Aspose.Imaging ροή δεδομένων για τεράστια TIFF;**  
A: Ναι—η βιβλιοθήκη γράφει κάθε καρέ απευθείας στο ρεύμα εξόδου, διατηρώντας τη χρήση μνήμης χαμηλή ακόμη και για χιλιάδες σελίδες.

**Q: Πώς εφαρμόζω προσωρινή άδεια προγραμματιστικά;**  
A: Φορτώστε το αρχείο `.lic` με `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.

**Q: Υπάρχει τρόπος να προεπισκοπήσετε το TIFF πριν την αποθήκευση;**  
A: Μπορείτε να αποδώσετε κάθε `TiffFrame` σε ένα `BufferedImage` και να το εμφανίσετε σε ένα στοιχείο Swing.

**Q: Ποιες εκδόσεις Java υποστηρίζονται επίσημα;**  
A: Το Aspose.Imaging υποστηρίζει Java 8 έως Java 21, συμπεριλαμβανομένων των εκδόσεων LTS.

## Συμπέρασμα

Τώρα έχετε μια πλήρη, έτοιμη για παραγωγή ροή εργασίας για τη δημιουργία πολυ‑σελίδων αρχείων TIFF με **ccittfax3 compression java** χρησιμοποιώντας το Aspose.Imaging. Ακολουθώντας τα παραπάνω βήματα, μπορείτε να αρχειοθετήσετε αποδοτικά τεράστιες συλλογές εγγράφων διατηρώντας το κόστος αποθήκευσης χαμηλό και την ποιότητα της εικόνας υψηλή. Εξερευνήστε πρόσθετες δυνατότητες του Aspose.Imaging—όπως OCR, διαχείριση μεταδεδομένων και μετατροπή μορφών—για να ενισχύσετε περαιτέρω τη διαδικασία επεξεργασίας εγγράφων.

---

**Τελευταία ενημέρωση:** 2026-09-28  
**Δοκιμή με:** Aspose.Imaging 25.5 for Java  
**Συγγραφέας:** Aspose

## Σχετικά Σεμινάρια

- [Πώς να δημιουργήσετε πολυ‑σελίδων TIFF με το Aspose.Imaging για Java – Ένας πλήρης οδηγός](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Πώς να μειώσετε το μέγεθος αρχείου εικόνας με συμπίεση LZW σε Java](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Διαχωρισμός καρέ πολυ‑σελίδων TIFF με το Aspose.Imaging για Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
---
date: '2026-07-17'
description: Μάθετε πώς να ορίσετε DPI στις εξαγωγές PDF χρησιμοποιώντας το Aspose.Imaging
  for Java, εξασφαλίζοντας υψηλής ποιότητας ανάλυση εικόνας κατά τη μετατροπή TIFF
  σε PDF.
keywords:
- set DPI PDF export Java
- Aspose.Imaging for Java
- TIFF to PDF conversion
- configure DPI in PDF export Java
- format conversion & export
lastmod: '2026-07-17'
og_description: Πώς να ορίσετε DPI στις εξαγωγές PDF χρησιμοποιώντας το Aspose.Imaging
  for Java. Ακολουθήστε αυτόν τον οδηγό βήμα-βήμα για να διατηρήσετε την ποιότητα
  της εικόνας κατά τη μετατροπή αρχείων TIFF σε PDF.
og_image_alt: Guide showing DPI settings in PDF export with Aspose.Imaging for Java
og_title: Πώς να ορίσετε DPI στις εξαγωγές PDF με το Aspose.Imaging for Java
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to set DPI in PDF exports using Aspose.Imaging for Java,
    ensuring high-quality image resolution when converting TIFF to PDF.
  headline: How to Set DPI in PDF Exports with Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to set DPI in PDF exports using Aspose.Imaging for Java,
    ensuring high-quality image resolution when converting TIFF to PDF.
  name: How to Set DPI in PDF Exports with Aspose.Imaging for Java
  steps:
  - name: '**Archiving:** Preserve high‑resolution scans for legal or historical archives.'
    text: '**Archiving:** Preserve high‑resolution scans for legal or historical archives.'
  - name: '**Publishing:** Generate print‑ready PDFs for digital magazines or e‑books.'
    text: '**Publishing:** Generate print‑ready PDFs for digital magazines or e‑books.'
  - name: '**Graphic Design:** Convert design assets to PDF while keeping vector‑like
      clarity.'
    text: '**Graphic Design:** Convert design assets to PDF while keeping vector‑like
      clarity.'
  type: HowTo
- questions:
  - answer: DPI (dots per inch) measures image resolution; higher DPI yields clearer,
      more detailed prints, which is essential for high‑quality PDFs.
    question: What is DPI and why does it matter?
  - answer: No – DPI is baked into the PDF at export time. To alter it, re‑export
      the source TIFF with a new DPI setting.
    question: Can I change the DPI after the PDF is created?
  - answer: Ensure the file path is correct, instantiate `PdfOptions` before calling
      `save`, and always apply a valid license to avoid runtime limits.
    question: What common pitfalls should I avoid when setting DPI?
  - answer: Yes – Aspose.Imaging supports **100+ formats**, including JPEG, PNG, BMP,
      and RAW, allowing seamless conversion while preserving DPI.
    question: Does Aspose.Imaging support other formats besides TIFF?
  - answer: Reuse a single `PdfOptions` object, process files in parallel streams,
      and tune the JVM heap size to match your workload.
    question: How can I improve conversion speed for large batches?
  type: FAQPage
tags:
- set dpi
- Aspose.Imaging
- Java image processing
- TIFF to PDF
- PDF export
title: Πώς να ορίσετε DPI στις εξαγωγές PDF με το Aspose.Imaging for Java
url: /el/java/format-conversion-export/set-dpi-pdf-export-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Πώς να ορίσετε DPI στις εξαγωγές PDF χρησιμοποιώντας το Aspose.Imaging για Java

## Εισαγωγή

**How to set dpi** είναι μια συχνή ερώτηση για προγραμματιστές που χρειάζονται καθαρά, έτοιμα για εκτύπωση PDF από υψηλής ανάλυσης TIFF. Σε αυτόν τον οδηγό θα μάθετε ακριβώς πώς να ορίσετε DPI στις εξαγωγές PDF με το Aspose.Imaging για Java, διατηρώντας την ποιότητα της εικόνας αμετάβλητη κατά τη μετατροπή TIFF σε PDF. Θα περάσουμε από τις προαπαιτούμενες συνθήκες, τη ρύθμιση των εξαρτήσεων και τη συγκεκριμένη ροή κώδικα που πρέπει να υλοποιήσετε.

## Γρήγορες Απαντήσεις
- **What is the primary class for PDF export?** `PdfOptions` configures resolution, compression, and other PDF‑specific settings.  
- **Which method loads a TIFF image?** `Image.load("file.tiff")` creates an in‑memory image object.  
- **How many DPI values can you set?** Any integer value; typical print quality uses 300 dpi or 600 dpi.  
- **Do I need a license for production?** Yes—Aspose.Imaging requires a valid license for unlimited usage.  
- **What Maven coordinates are required?** `com.aspose:aspose-imaging:25.5` or newer.

## Τι είναι το «how to set dpi»;
«how to set dpi» αναφέρεται στη διαμόρφωση της ανάλυσης σε κουκκίδες ανά ίντσα (dots‑per‑inch) μιας εικόνας όταν αυτή αποθηκεύεται ή εξάγεται, επηρεάζοντας άμεσα την ευκρίνεια του τελικού εγγράφου. Η ρύθμιση αυτής της τιμής καθορίζει πόσες εικονοστοιχεία εκτυπώνονται ανά ίντσα, κάτι που είναι κρίσιμο για την επίτευξη επαγγελματικής ποιότητας εκτύπωσης και για την αποφυγή απώλειας λεπτομερειών κατά τη μετατροπή.

## Γιατί να ορίσετε DPI κατά την εξαγωγή PDF;
Η ρύθμιση DPI εγγυάται ότι το PDF διατηρεί τις αρχικές λεπτομέρειες της εικόνας. Το Aspose.Imaging επεξεργάζεται **πάνω από 100 μορφές εικόνας** και μπορεί να χειριστεί έγγραφα με εκατοντάδες σελίδες χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, προσφέροντας **30 % ταχύτερη μετατροπή** σε σύγκριση με γενικές βιβλιοθήκες. Επιπλέον, η σωστή ρύθμιση DPI αποτρέπει ανεπιθύμητα σφάλματα κλιμάκωσης και εξασφαλίζει ότι το εκτυπωμένο αποτέλεσμα ταιριάζει με τις προσδοκίες στην οθόνη.

## Προαπαιτούμενα

- **Aspose.Imaging for Java** έκδοση 25.5 ή νεότερη.  
- Java Development Kit (JDK) 11 ή νεότερο.  
- IDE όπως IntelliJ IDEA ή Eclipse.  
- Βασικές γνώσεις Java και εξοικείωση με τη διαχείριση εικόνων.

## Ρύθμιση του Aspose.Imaging για Java

### Maven
Προσθέστε την ακόλουθη εξάρτηση στο αρχείο `pom.xml` σας:
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle
Συμπεριλάβετε αυτή τη γραμμή στο αρχείο `build.gradle` σας:
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Άμεση Λήψη
Εναλλακτικά, κατεβάστε τη νεότερη βιβλιοθήκη Aspose.Imaging για Java από τις [Ανακοινώσεις Aspose.Imaging](https://releases.aspose.com/imaging/java/). Μπορείτε επίσης να ανατρέξετε στις [Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/) για ιστορικό εκδόσεων και changelogs.

#### Βήματα Απόκτησης Άδειας
- **Free Trial:** Ξεκινήστε κατεβάζοντας μια δωρεάν δοκιμή για να δοκιμάσετε τις δυνατότητες.  
- **Temporary License:** Αιτηθείτε προσωρινή άδεια στην ιστοσελίδα Aspose εάν χρειάζεστε περισσότερο χρόνο πέρα από την περίοδο δοκιμής.  
- **Purchase:** Για μακροπρόθεσμη χρήση, εξετάστε την αγορά άδειας.

## Οδηγός Υλοποίησης

### Πώς να ορίσετε DPI στην εξαγωγή PDF χρησιμοποιώντας το Aspose.Imaging για Java;

Φορτώστε το TIFF, διαμορφώστε το `PdfOptions` με το επιθυμητό DPI και καλέστε `save` – αυτό ολοκληρώνει τη μετατροπή σε τρία σύντομα βήματα. Η προσέγγιση διατηρεί την πιστότητα της εικόνας και λειτουργεί για οποιοδήποτε μέγεθος TIFF, από μονή σελίδα έως πολυσελιδή έγγραφα. Ορίζοντας ρητά τις ιδιότητες `resolutionX` και `resolutionY` στο `PdfOptions`, ελέγχετε το DPI εξόδου, διασφαλίζοντας ότι το παραγόμενο PDF ταιριάζει με την επιθυμητή ποιότητα εκτύπωσης.

#### Φόρτωση της Εικόνας
Η κλάση `Image` είναι το βασικό αντικείμενο του Aspose.Imaging που αντιπροσωπεύει μια ραστερική εικόνα στη μνήμη. Η φόρτωση σας δίνει πρόσβαση σε ιδιότητες πλάτους, ύψους και ανάλυσης.
```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffImage;

String filePath = "YOUR_DOCUMENT_DIRECTORY/Tiff/AFREY-Original.tif";  // Replace with your TIFF directory path

TiffImage tiffImage = (TiffImage) Image.load(filePath);
```

#### Αρχικοποίηση Επιλογών Εξαγωγής PDF
`PdfOptions` είναι η κλάση διαμόρφωσης που ορίζει πώς μια εικόνα γράφεται σε PDF, συμπεριλαμβανομένου του DPI, της συμπίεσης και του μεγέθους σελίδας.
```java
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.ResolutionSetting;

PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setResolutionSettings(new ResolutionSetting(
        tiffImage.getHorizontalResolution(),   // Get horizontal DPI from TIFF
        tiffImage.getVerticalResolution()));  // Get vertical DPI from TIFF
```

#### Αποθήκευση της Εικόνας ως PDF
Η μέθοδος `save` στο αντικείμενο `Image` γράφει την επεξεργασμένη εικόνα σε αρχείο PDF χρησιμοποιώντας τις επιλογές που παρείχατε.
```java
String outDir = "YOUR_OUTPUT_DIRECTORY/Tiff/";  // Replace with your desired output directory path

tiffImage.save(outDir + "/result.pdf", pdfOptions);
```

### Καθαρισμός: Διαγραφή Προσωρινών Αρχείων
Μετά την επεξεργασία, αφαιρέστε τυχόν ενδιάμεσα αρχεία για να ελευθερώσετε χώρο στο δίσκο και να αποφύγετε ακαταστασία.
```java
import java.io.File;

File file = new File(outDir + "/result.pdf");
if (file.exists()) {
    file.delete(); // Remove the file from the output directory
}
```

## Πρακτικές Εφαρμογές

1. **Αρχειοθέτηση:** Διατήρηση υψηλής ανάλυσης σκαναρισμάτων για νομικά ή ιστορικά αρχεία.  
2. **Δημοσίευση:** Δημιουργία έτοιμων για εκτύπωση PDF για ψηφιακά περιοδικά ή e‑books.  
3. **Γραφιστικός Σχεδιασμός:** Μετατροπή σχεδιαστικών στοιχείων σε PDF διατηρώντας καθαρότητα παρόμοια με διανυσματική.

## Παρατηρήσεις Απόδοσης

- **Διαχείριση Μνήμης:** Χρησιμοποιήστε try‑with‑resources για αυτόματο κλείσιμο ροών και μείωση πίεσης στο heap.  
- **Ρύθμιση JVM:** Αυξήστε το `-Xmx` εάν επεξεργάζεστε πολύ μεγάλες TIFF· το Aspose.Imaging ροές δεδομένων αποδοτικά, αλλά μεγάλες εικόνες απαιτούν επαρκή χώρο heap.  
- **Επεξεργασία Μαζικής Επεξεργασίας:** Επαναχρησιμοποιήστε ένα ενιαίο αντικείμενο `PdfOptions` όταν μετατρέπετε πολλά αρχεία για μείωση του κόστους δημιουργίας αντικειμένων έως και 20 %.

## Συμπέρασμα

Τώρα γνωρίζετε **πώς να ορίσετε dpi** για εξαγωγές PDF με το Aspose.Imaging για Java, διασφαλίζοντας ότι κάθε PDF που δημιουργείτε διατηρεί την αρχική ευκρίνεια της εικόνας. Εφαρμόστε αυτά τα βήματα στα δικά σας έργα και θα παράγετε σταθερά επαγγελματικής ποιότητας PDF χωρίς επιπλέον επεξεργασία.

---

## Συχνές Ερωτήσεις

**Ε: Τι είναι το DPI και γιατί είναι σημαντικό;**  
Α: Το DPI (dots per inch) μετρά την ανάλυση της εικόνας· υψηλότερο DPI προσφέρει πιο καθαρά, πιο λεπτομερή εκτυπώσεις, κάτι που είναι ουσιώδες για υψηλής ποιότητας PDF.

**Ε: Μπορώ να αλλάξω το DPI μετά τη δημιουργία του PDF;**  
Α: Όχι – το DPI ενσωματώνεται στο PDF κατά τη στιγμή της εξαγωγής. Για να το αλλάξετε, πρέπει να εξάγετε ξανά το αρχικό TIFF με νέα ρύθμιση DPI.

**Ε: Ποιες κοινές παγίδες πρέπει να αποφύγω όταν ορίζω DPI;**  
Α: Βεβαιωθείτε ότι η διαδρομή του αρχείου είναι σωστή, δημιουργήστε το `PdfOptions` πριν καλέσετε `save` και εφαρμόστε πάντα έγκυρη άδεια για να αποφύγετε περιορισμούς χρόνου εκτέλεσης.

**Ε: Υποστηρίζει το Aspose.Imaging άλλες μορφές εκτός του TIFF;**  
Α: Ναι – το Aspose.Imaging υποστηρίζει **πάνω από 100 μορφές**, συμπεριλαμβανομένων JPEG, PNG, BMP και RAW, επιτρέποντας απρόσκοπτη μετατροπή διατηρώντας το DPI.

**Ε: Πώς μπορώ να βελτιώσω την ταχύτητα μετατροπής για μεγάλες δέσμες αρχείων;**  
Α: Επαναχρησιμοποιήστε ένα ενιαίο αντικείμενο `PdfOptions`, επεξεργαστείτε αρχεία σε παράλληλες ροές και ρυθμίστε το μέγεθος heap της JVM ώστε να ταιριάζει στο φορτίο εργασίας σας.

## Πόροι

- **Τεκμηρίωση:** [Aspose.Imaging for Java](https://reference.aspose.com/imaging/java/)
- **Λήψη:** [Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/)
- **Αγορά:** [Buy Aspose.Imaging](https://purchase.aspose.com/buy)
- **Δωρεάν Δοκιμή:** [Aspose.Imaging Free Trial](https://releases.aspose.com/imaging/java/)
- **Προσωρινή Άδεια:** [Get a Temporary License](https://purchase.aspose.com/temporary-license/)
- **Υποστήριξη:** [Aspose Imaging Forum](https://forum.aspose.com/c/imaging/14)

**Last Updated:** 2026-07-17  
**Tested With:** Aspose.Imaging for Java 25.5  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Extract and Set PNG Resolution in Java with Aspose.Imaging](/imaging/java/format-specific-operations/master-png-resolution-aspose-imaging-java/)
- [Aspose.Imaging Java: Configure BMP Options for Optimal Image Processing](/imaging/java/format-specific-operations/aspose-imaging-java-set-bmp-options/)
- [java image resolution – Master Image Resolution Alignment with Aspose.Imaging for Java](/imaging/java/image-processing-and-enhancement/image-resolution-alignment/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}